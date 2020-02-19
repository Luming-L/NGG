| Organism | Size | contig<br>number | contig<br>N50 | Scaffold<br>number | estimated completeness | 
| :------------: | :------------: |  :------------: | :------------: | :------------: | :------------: | 
|Nymphaea colorata|409 Mb| 1429 | 2.1 Mb| 804 | 94.4%

## sequencing
Genome sequencing
PacBio RSII single-molecule real-time (SMRT) sequencing technology
20kb SMRTbell libraries
34 SMRT cells
49.8 Gb 5.5 million reads

transcriptome sequencing 
Illumina platform 
paired-end reads

Hi-C sequencing and scaffolding 
illumina platform

## assembly
remove organellar DNA, reads of poor quality or short length, and chimaeras 
contig-level assembly 
Polish the draft assembly
increase the accuracy of the assembly
measure genome assembly quality
map Hi-C paired-end reads to draft asssembly contigs, group into chromosomes and scaffold 
full PacBio long reads after filtered - Canu v.1.3 for self-correction and assembly 
draft assembly - Arrow
increase the accuracy of the assembly - Illumina short reads + Pilon
genome assembly - BUSCO (Benchmarking Universal Sin-
gle-Copy Orthologues)23 v.3.0.
Hi-C paired-end reads - Lachesis

```mermaid
graph TD
P[PacBio long reads]-.->A
I[Illumina short reads]-.->B

subgraph 
A[Canu]-->B[Arrow polishing]
B[Arrow polishing]-->C[Pilon Polishing]
C[Pilon Polishing]-->D[HiC pro]
D-->E[Lachesis]
end 

```

## annotation
Genscan
Augustus A.thaliana
MAKER

reads 
contig
scaffold
N50
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0ODAyOTYyMTAsMjM0MDQzMjI3LDI1OT
QxNDU3NSwtMzQyODE0NTAxLDEwMzg5Nzc3NzEsMjAzNDMwMDE5
NCwtNzI2MjgxMTAxLDYzMzUxNTIxMCwxMzU2MTg0MjUxLC0xNT
M0MjcyMTgxLDE0OTUxMDU0MjAsLTIwMzc1Mjc0MiwtMTUwNDMz
NDExMywtNjQ2NDg1NDMxLDQ5NzgxODgxMF19
-->