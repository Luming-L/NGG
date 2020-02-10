## overlap graph
## **De Bruijn graph** 
split reads into k-mers
build graph of k-mers
deconvolute graph to derive assembly: Eulerian cycle problem
**Error (Tips and bubbles) removal**
**Velvet**: twin node block arcs 

> 
## how de Bruijn graph are simplified


node - read
hamoteneous problem

NP problem 

de bruijn graph:
node - k-mer
deal with repeat
software: Velvet
error produce tips in graph

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
eyJoaXN0b3J5IjpbNDM4NzMxMjA5LDE0NDMwMDM5NDMsLTE0MT
AyMjQ4MywtMjA0NjA5NDk4MSwtOTQwOTY2NDM2LC0xOTY3OTEx
Mzc4LDIwOTY0MTc0MjIsMjAwMDExODI4MywxMjQzNTczNDk3XX
0=
-->