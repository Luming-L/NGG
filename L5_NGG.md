## Overlap graph OLC
1. identify overlaps of reads
2. build graph of reads
	* each k-mer is a node
3. build consensus sequence
NP complete？
Hamiltonian Path identified？
## De Bruijn graph
1. split reads into k-mers
2. build graph of k-mers
	* each k-mer is a node
	* directed edges from one node to another indicate overlaps
	* Simplification of linear stretches?
	* Error (tip and bubble removal)?
3. deconvolute graph to derive assembly
	* Eulerian cycle problem
## Velvet
twin node?
reverse complement k-mers
## Repeat

## Simplified de Bruijn graph
When a node A has only one outgoing arc that points to another node B that has only one ingoing arc, merge these two nodes.
## Error removal
* tips - errors at the edges of reads
> A tip is a chain of nodes that is disconnected on one end
> remove tips
* bubbles - internal read errors or nearby tips connecting
> two paths are redundant and contain similar sequence
* erroneous connections - technical errors or distant tips merging
> After the above corrections, genuine short nodes that cannot be simplified correspond to low-complexity sequences that present multiple times in the genome.
> It is likely that any low coverage node left after tip and bubble resolution is a chimeric connection, due to spurious overlaps created by experimental errors.
split reads into k-mers

for each k-mer, extract it from left and right to get two (k-1)-mers
each unique (k-1)-mer is a node
each k-mer is a directed edge 
walk through **each** directed edge only **once** (Eulerian cycle problem)




deploid - nucleopholyphorism - two alleles
deploid aware assembler

haplotic
graph to many actual sequences (contigs)

8 bridges able to cross once


## Assessing genome assembly quality




 


 
 scaffolding DNA
 small trunck of DNA 
 contig
 10x the same
 Optical Mapping: cut at specific motif microscopy
 Genetic Mapping:
 pacbio error prone

## pipeline

 short reads can increase resolution 
 error correct 

## assembly numerical metrics
- "N" 
	+ the number of uncertain bases
	+ caused by uncalled bases/unsequenced gaps/unresolved errors
- Number of contigs/scaffolds
	+ lots of contigs - many repeats
	+ compared to the number of chromosomes, the number of scaffolds should be close to that of chromosomes.
	+ good: 2 contigs map the scaffold from two sides (center is centromere and thus has many repeats)
	+ bad: hundread of contigs set to a chromosome
* N50 (contig/scaffold N50 length)
	+ length of contigs/scaffolds (compared to the size of the genome)
	+ N50:  the length of contig at which half the assembly is in contigs of that size or greater
- Busco and cegma 
	+ higher percentage more complete
> Snail plots https://github.com/rjchallis/assembly-stats
## long-range scaffolding approaches
Motivation: Repeats can only be resolved if the sequencing technology used to generate the raw data for assembly has a working span longer than the repeat length.
Repeats have many different families.
- read pairs
- mate pairs
	+ single paired read at each side
- RNA-seq
	+ the transcript assembly spans the repetitive region
	+ DNA - assembly, RNA - annotation
- Proximity ligation
	+ HiC: sequencing of chimaeric fragments derived from proximity ligation of nuclear DNA
	+ Chicago: in vitro reconstituted chromatin
- Synthetic long reads
	+ 10x Genomics
		1.  mid-tagged library?
- Optical mapping
- Radiation hybrid mapping
- Genetic mapping
- Long reads
## how long reads can be used to improve assemblies
## technologies used for long read assembly

## Definition
**Contig:**
- Contig means "contiguous". 
- In genome assembly, a contig is a series of overlapping reads that reconstruct the original DNA sequence of a chromosome or a region of a chromosome. 
- Contigs only contains A, T, C, or G bases without gaps.

**Scaffold:**
- Scaffold chains contigs together.
- Need additional information about the relative position and orientation of the contigs in the genome.
- Contigs in a scaffold are separated by gaps (indicated by "N"s)
- optical mapping, crosslinking, and so on.




[https://www.genome.gov/genetics-glossary/Contig](https://www.genome.gov/genetics-glossary/Contig)
[https://www.pacb.com/blog/genomes-vs-gennnnes-difference-contigs-scaffolds-genome-assemblies/](https://www.pacb.com/blog/genomes-vs-gennnnes-difference-contigs-scaffolds-genome-assemblies/)
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDAwMzg3NjU4LDEwNjcyNTI2NTMsLTE2OD
Q1NzM2NjQsLTE4MzMwODE1Miw2MTU1NjgxNTksLTE1NTIyOTA3
MzcsMTM1NDkwMjYyMCwtMzQyOTI2MDk2LDI3OTc5NjA4NCwxOD
M5Njg2NjU2LC0xMDE4MTM5NjA2LC03MzgyNTE4Niw4MjY2NzY3
NzYsNDcxNzc4NDUyLDE3OTIxOTkwMzEsLTE3NjQ1NzQ1NjcsNj
A5MzUzOTQsLTIyMjE2NzEwNCwxNzEwOTUzNDE4LDEzOTc5MDc1
MTJdfQ==
-->