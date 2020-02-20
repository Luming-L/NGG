## PacBio Single Molecule, Real-Time sequencing (SMRT)
good for de novo Genome Assembly

### Process of SMRT:
- single molecule
	+ ligate adapters to double strand DNA to create circular template
	+ immobilize DNA polymerase with a single molecule of DNA template and primer to a ZMW (zero-mode waveguides; tiny wells in a SMRT cell; each cell contains millions of ZMWs)
- real-time
	+ nucleotides attached with fluorescent dyes
	+ detect the fluorescent signal of the nucleotide incorporated by the DNA polymerase as DNA is synthesized
> [smrt sequencing](https://www.pacb.com/smrt-science/smrt-sequencing/)

### advantages 
- Long Reads
	+ reads tens of kilobases in length	
	+ assemble complete genomes and sequence full-length transcripts
- High Accuracy
	+ Sequencing free of systematic error achieves >99.999% consensus accuracy.
- Uniform Coverage
	+ No bias based on GC content means you can sequence through region inaccessible to other technologies.
- Single-Molecule Resolution
	+ Capturing sequence data from native DNA or RNA molecules enables highly accurate long reads with >99% single-molecule accuracy.
- Epigenetics
	+ With no PCR amplification step, base modifications are directly detected during sequencing.

### why select this approach
- Plant genomes are more repetitive and complicate to assemble than vertebrates.
- Long-read assembly contigs outperform short-read assembly scaffolds.
- Long-range scaffolding can advance assembly contiguity up to chromosomal levels.
- Reconstruction of haplotypes allows assembly of heterozygous and polyploid genomes.

The contiguity of assembly from next generation sequencing data is relatively low. Third generation sequencing can produce long reads to cover these gaps.

Only the minority of the plant genome assemblies are on chromosome-level. Most of them are based on short-read sequencing and consist of hundreds or even thousands of fragmented contigs and scaffolds, which are usually not mapped to their chromosomal locations.

High repetitiveness due to transposable elements, extreme genome sizes (loblolly pine, Norway spruce) and the polyploid nature of some plants. 

long-read sequencing and long-range scaffolding methods such as optical mapping, chromosome conformation capture, and DNA dilution-based technologies were introduced to overcome the weaknesses of short-read assemblies and ultimately to enable the assembly of entire chromosomes.

>[all plant genomes](https://www.plabipd.de/plant_genomes_pa.ep)

> [The impact of third generation genomic technologies on plant genome assembly](https://www.sciencedirect.com/science/article/pii/S1369526616301315#!)

> [Original publication](https://science.sciencemag.org/content/323/5910/133/tab-pdf)

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0NzAxMDMxNjIsMTE4MzEzNDQzNiwxMD
M0MjQ5NDQyLDUyNjY1MDg5MSwtMzU2OTczMTI2LDY5MDQ3Mjgw
NSwzNzA2MTE2NzksMTAyNTUwNjE0OCwtMzQ0MjI1OTk5LC0zNT
QxMjc1MTQsMTYzOTAzNDMxNCwtMTQ5Njg0NzYwNCwxMDQzNjU1
NTE4LC0xNTg3ODgxNDU2LC0yMTE5NzYwOTc4XX0=
-->