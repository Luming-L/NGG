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
De novo long-read genome assembly involves in several steps:
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
eyJoaXN0b3J5IjpbLTEwMDIwOTE2NjQsMTY4ODYxNjc3MywtMT
U1NTUxNTM2LDE1NjIwNDc1NywxNTYyMDQ3NTcsODgxMjUwMzc0
LC0zNjAzNjM2NTIsLTE5ODAxNDQxNDUsOTQ1OTE3ODk5LC0xNz
kyMTcxOTc0LDU2NTkyNjM2MiwxNDI1Njc4NDUwLDc0MzYxNTkz
NCwyMTIxNTQxMTM1LDEzMzA1MTQ1MzksNDUyMDAwNjk5LDIyND
IwNTUzNyw3MzA5OTgxMTZdfQ==
-->