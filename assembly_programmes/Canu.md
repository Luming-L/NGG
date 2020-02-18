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
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY3MTEyMjE2OSw1MzE5MTQzMzgsMzUwMT
g3NDk3LDEwNzIyNjY3MTQsMjA1OTA3MjEyMiwtOTUxMTQ2OTYw
LC0xMzQxMzAxNDQ5LC0xNTg5MDYzNTAwLDE2ODM5OTIxNDYsLT
MwODMxMV19
-->