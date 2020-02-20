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

## Long-read sequencing technologies
Sequencing error rates of raw reads are relatively high, but self-correction with sufficient sequencing data or correction by short sequencing reads can improve sequence accuracy to over 99.999%.
In addition to contiguity, PacBio assembly contigs feature less gaps (represented as Ns in the sequence) and their overall lengths includes more of the genomic space. 

## Long-range scaffolding technologies
To improve assembly contiguity, the contigs of an assembly need to be scaffolded, which typically starts by ordering the contigs using alignments of paired reads.
Recently several novel technologies emerged, which promise to improve scaffolding and eventually eliminate the need for genetic or physical mapping.
Optical mapping generates fingerprints of DNA fragments of up to multiple hundred kb by imaging the patterns of restriction sites under light microscopes using fluorescently labeled enzymes.
Such individual fingerprints (or maps) can be assembled into genome-wide (consensus) maps, which can then be used to scaffold the contigs of a corresponding sequence assembly and identify large structural variations
The combination of sequencing data and optical maps works particularity well, as the typical breaks in sequence assemblies are at repeats, while optical map assemblies have a bias to break at regions with closely-spaced restriction sites.

Hi-C is based on proximity ligation of DNA fragments that are physically close in their natural conformation. 
Though not all DNA, which is in close proximity, is also closely linked, the majority of the read pairs generated from the two ends of such fragments comes from closely linked DNA and therefore these read pairs can be used for scaffolding.
A modified Hi-C protocol called Chicago is provided as a service by Dovetail Genomics since 2014.

## Assembly of heterozygous and polyploid genomes



>[all plant genomes](https://www.plabipd.de/plant_genomes_pa.ep)

> [The impact of third generation genomic technologies on plant genome assembly](https://www.sciencedirect.com/science/article/pii/S1369526616301315#!)

> [Original publication](https://science.sciencemag.org/content/323/5910/133/tab-pdf)

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwMTgzOTcxNDMsMTA5MTYxMTMzNyw3Mj
AzNjQwODcsMjExNDI0NDIxOSwtMTUxMjYyNTQ3Niw1MzIyMTEz
MTMsLTI1NzE2MjY1Nyw4Njc1Mzc2OTYsMTMwOTQ0NzIwNCwtNT
M2MTI5NzcxLC05NzMxMjgyMDgsLTE0NzAxMDMxNjIsMTE4MzEz
NDQzNiwxMDM0MjQ5NDQyLDUyNjY1MDg5MSwtMzU2OTczMTI2LD
Y5MDQ3MjgwNSwzNzA2MTE2NzksMTAyNTUwNjE0OCwtMzQ0MjI1
OTk5XX0=
-->