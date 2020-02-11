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



Busco and cegma higher percentage more complete
 different family of repeats 
 long repeat impossible to assemble
 mate pairs - single paired read at each side
 DNA assembly
 RNA - annotation
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

## assembly quality metrics
* Number of uncalled bases
> "N"s
> unsequenced gaps
> unresolved errors
* Number of contigs/scaffolds
> lots of contigs - many repeats
> compared to the number of chromosomes, the number of scaffolds should be close to that of chromosomes.
> good: 2 contigs from two sides (center is centromere and have many repeats)
> bad: hundread of contigs set to a chromosome
* Mean length of contigs/scaffolds (compared to the size of the genome)
> **N50** :  the length of contig at which half the assembly is in contigs of that size or greater
## long-range scaffolding approaches
## how long reads can be used to improve assemblies
## technologies used for long read assembly
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI3MTg2NDA1Miw0NzE3Nzg0NTIsMTc5Mj
E5OTAzMSwtMTc2NDU3NDU2Nyw2MDkzNTM5NCwtMjIyMTY3MTA0
LDE3MTA5NTM0MTgsMTM5NzkwNzUxMiwtMTUzODI1MDE5MiwtMT
QxNTMyMDU5NiwtMTgwNjI5NjYyNSwyMDEyNzI3NzcxLC0xOTEw
MDUyMjkxLC0xMTk3NzYwMDQsLTU3NTk0MzQ4NywtMTI0NTk4MT
kxMSwtNTc4NDI2NzExLDUzNjg1MTkwNSw0Mzg3MzEyMDksMTQ0
MzAwMzk0M119
-->