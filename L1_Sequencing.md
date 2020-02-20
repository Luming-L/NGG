## PacBio Single Molecule, Real-Time sequencing (SMRT)
good for de novo Genome Assembly

### Process of SMRT:
- library preparation
	+ ligate adapters to double strand DNA to create circular template
	+ immobilize DNA polymerase with a single molecule of DNA template and primer to a ZMW (zero-mode waveguides, tiny wells in a SMRT cell)
- sequencing
	+ add nucleotides attached with fluorescent dyes
	+ detect the fluorescent signal of the nucleotide incorporated by the DNA polymerase as DNA synthesizes
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

> [The impact of third generation genomic technologies on plant genome assembly](https://www.sciencedirect.com/science/article/pii/S1369526616301315#!)
[Original publication](https://science.sciencemag.org/content/323/5910/133/tab-pdf)

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzcwNjExNjc5LDEwMjU1MDYxNDgsLTM0ND
IyNTk5OSwtMzU0MTI3NTE0LDE2MzkwMzQzMTQsLTE0OTY4NDc2
MDQsMTA0MzY1NTUxOCwtMTU4Nzg4MTQ1NiwtMjExOTc2MDk3OF
19
-->