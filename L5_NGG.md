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


hundread of contigs set to a chromosome
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
> good: 2 contigs from two sides (center is centromere and have many repeats)
* Mean length of contigs/scaffolds
## long-range scaffolding approaches
## how long reads can be used to improve assemblies
## technologies used for long read assembly
<!--stackedit_data:
eyJoaXN0b3J5IjpbNjY2MTI5NDcyLDE3OTIxOTkwMzEsLTE3Nj
Q1NzQ1NjcsNjA5MzUzOTQsLTIyMjE2NzEwNCwxNzEwOTUzNDE4
LDEzOTc5MDc1MTIsLTE1MzgyNTAxOTIsLTE0MTUzMjA1OTYsLT
E4MDYyOTY2MjUsMjAxMjcyNzc3MSwtMTkxMDA1MjI5MSwtMTE5
Nzc2MDA0LC01NzU5NDM0ODcsLTEyNDU5ODE5MTEsLTU3ODQyNj
cxMSw1MzY4NTE5MDUsNDM4NzMxMjA5LDE0NDMwMDM5NDMsLTE0
MTAyMjQ4M119
-->