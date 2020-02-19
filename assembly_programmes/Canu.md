## Introduction
Genomic repeats longer than read length will disturb overlapping of reads. Single-molecule sequencing can produce reads > 10kb, but it is less accurate.

PacBio single-molecule real-time (SMRT) and Oxford Nanopore strand sequencing have their own characters and requirements for assembly. 

New approaches come out to deal with data with increased read length and error rate. These can be roughly categorised as hybrid, hierarchical or direct methods.

Hybrid methods rely on complementary short reads for accurate base calls.
**Hierarchical methods** use multiple rounds of read  overlapping (alignment) and correction to improve read quality prior to assembly.
Direct methods attempt to assemble from a single overlapping step without any prior correction.

Here focus on HM, because it has produced the most continuous de novo assemblies to date.

## Result
Canu introduces the MinHash Alignment Process (MHAP) to overlap noisy, single-molecule sequencing reads better.

Characters of Canu (results):
- support both PacBio and Oxford Nanopore data
- lower runtime and coverage requirements
- improve repeat and haplotype separation

Novel features (techniques):
- computational resource discovery
- adaptive k-mer weighting
- automated error rate estimation
- sparse graph construction
- graphical fragment assembly (GFA)

Three stage:
- correction
- trimming
- assembly

just require 20000 CPU hours to assemble a human genome

**Adaptive MinHash k-mer weighting**
Repeats not only fragment assemblies, but also disrupt overlapping.
Two stages in read overlapping:
1. build a list of read pairs with some similarity
2. perform a more direct comparison of them
In the first step, identify shared k-mers between all pairs of reads to find candidate overlaps. Repeats will disrupt overlapping because: 
repeats - frequent occurrence of some k-mers - increase the number of candidate overlaps - more complex second stage
A solution for this: mask low-complexity sequence or ignore highly repetitive k-mers to induce indexing. (Celera Assembler, FALCON, Miniasm)
Problem caused: some overlaps will not be detected

Can reduce but not eliminate selecting a repetitive k-mer for overlapping
A repetitive k-mer occurring many times throughout the genome - reduced weight 
A relatively unique k-mer occurring multiple times in a single read - increased weight 
known as a tf-idf weight (term frequency, inverse document frequency)

The weighting is the number of occurrences of a k-mer inside a read (the document) and the overall rarity of the k-mer among all reads (the corpus)
This method reduces the number of uninformative, repetitive overlaps that are identified, improving runtime and memory usage significantly.

Traditional strategies filter fixed, all-or-nothing threshold.
Adaptive MinHash k-mer weighting can divide repeats into different groups. Repeats from plasmids can be taken into account, but the number of false positive overlaps induced by repeat will not increase.
Canu don't require parameter adjustment (the threshold to filter repetitive k-mers) and achieve high sensitivity (when the threshold is low it is not sensitive) and maintains high positive predictive value (high threshold causes false positive) with no added runtime or memory penalty (Checking overlaps in case of false positive will increase runtime and memory penalty).

Best overlap graph
Canu was a variant of the greedy "Best overlap graph" (BOG) algorithm
Only load the "bet"
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTAwMDIyOTMsLTcwMTQ1OTM2LC0xODMxNz
MzNjgxLDE4OTQ2NjE3MTAsNTMxOTE0MzM4LDM1MDE4NzQ5Nywx
MDcyMjY2NzE0LDIwNTkwNzIxMjIsLTk1MTE0Njk2MCwtMTM0MT
MwMTQ0OSwtMTU4OTA2MzUwMCwxNjgzOTkyMTQ2LC0zMDgzMTFd
fQ==
-->