The bioinformatics tools for the genome assembly and
analysis based on third-generation sequencing

## Keywords
- Bioinformatics tools
- third-generation sequencing
- genome assembly
- genome sequencing

We review a total of 39 TGS analysis tools, which were either recently published or developed (TableS1).
We discuss their various characteristics,such as the required input, interaction with the user, sequencing platforms,type of reads, error models, possibility of introducing coverage bias, simulation of genomic variants and output provided.
This review evaluates various tools applied in three main TGS platforms on genome assembly and further analysis.
Details of each approach along with its benefits and drawbacks are discussed. 
Two distinct decision trees are presented to guide researchers for selecting a suitable TGS de novo and genome-based sequencing analysis tools.
## De novo assembly using TGS technologies
### Steps in de novo long-read genome assembly
- preassembly
	- raw read mapping
	- read error correction
		- align long reads against themselves
		- use short reads to correct long reads 
- assembly of corrected reads
	- algorithm
		- overlap-layout-consensus (OLC)
		- de Bruijn graphs (DBG)
		- string graphs
- assembly polishing
	- use short or long reads
	- solve indels and substitutions

### Tools for SMRT
- MinHash Alignment Process (MHAP)
	- identify all overlaps among noisy long reads
	- use a probabilistic Hashing algorithm
	- The algorithm works by estimating the Jaccard similarity based on the minimum k-mers
	- index, store, hash, compare k-mers
- PBJelly
	- use scaffolding approach for gap closing
- Hierarchical Genome-Assembly Process (HGAP)
	- apply the longest reads for assembling a sequence genome
- FALCON
	- hierarchical haplotype genome assembly
	- utilize more computationally optimized elements
- HINGE 
	- OLC paradigm
	- not error correction
- Minimap/miniasm
- Circlator
- Canu

Both HGAP and PBJelly are applicable for bacterial-sized genomes and MHAP is used in eukaryotic-sized genomes. 

for all overlap
overlap-based procedures such as overlap-layout-consensus (OLC) algorithms
- generate alignments between long reads
- calculate the best overlap graph
- generate the consensus sequence of the contigs from the graph
### Genome alignment and assembly tools for TGS platform
### Sequencing tools for hybrid technologies of both NGS and TGS

## Tools for genome-based sequence analysis
platform
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyNDAxNzA3MjcsLTEzMDExMjI0NDQsMT
gxNzA2MTE3NCwtNTQ2MjE0OTMwLDMxNDY4NzExNSwtMjE0MTAx
MzM4OCwtMTUwMDUyMzM0MiwxNDc3MDkxMjMwLDg3OTYyNjg5NS
wyMTA4ODA1Mjk5LDM1NzEzNDYzNCwtMTcyOTUxNDY4MCwtMTAw
MjA5MTY2NCwxNjg4NjE2NzczLC0xNTU1NTE1MzYsMTU2MjA0Nz
U3LDE1NjIwNDc1Nyw4ODEyNTAzNzQsLTM2MDM2MzY1MiwtMTk4
MDE0NDE0NV19
-->