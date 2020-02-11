## Overlap graph OLC
Hamiltonian Path identified
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

deconvolute graph to derive assembly: Eulerian cycle problem
**Error (Tips and bubbles) removal**
**Velvet**: twin node block arcs 


NP problem 
deploid - nucleopholyphorism - two alleles
deploid aware assembler

haplotic
graph to many actual sequences (contigs)

8 bridges able to cross once
poping bubbles trimming tips

## Assessing genome assembly quality
lots of contigs - many repeats
2 contigs from two sides 
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

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQyMjU0Njk2NSwtMjIyMTY3MTA0LDE3MT
A5NTM0MTgsMTM5NzkwNzUxMiwtMTUzODI1MDE5MiwtMTQxNTMy
MDU5NiwtMTgwNjI5NjYyNSwyMDEyNzI3NzcxLC0xOTEwMDUyMj
kxLC0xMTk3NzYwMDQsLTU3NTk0MzQ4NywtMTI0NTk4MTkxMSwt
NTc4NDI2NzExLDUzNjg1MTkwNSw0Mzg3MzEyMDksMTQ0MzAwMz
k0MywtMTQxMDIyNDgzLC0yMDQ2MDk0OTgxLC05NDA5NjY0MzYs
LTE5Njc5MTEzNzhdfQ==
-->