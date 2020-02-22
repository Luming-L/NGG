
Comprehensive evaluation of 
non-hybrid genome assembly tools for 
third-generation PacBio long-read sequence data

non-hybrid genome assembly tools
10 long-read assemblers
different taxonomic categories 
different genome size



## Long-read assembly pipelines
algorithms for de novo assembly 
- Overlap layout consensus (OLC) approach 
- de Bruijn graphs 
- string graphs 
SMS data has the high error rates. Hence, de Bruijn graphs was unfeasible, OLC approach and the string graphs are more suitable.
Currently, most long-read OLC pipelines follow a hierarchical approach: use single-molecule sequencing data for long reads correction. 
- select a subset of longer read
> [assembler evaluation](https://academic.oup.com/bib/article/20/3/866/4590140)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTMyOTkwNTYyNSw2MzE5NDU0NjEsNzU0OD
QzMjgxLDQyMTcwODQyNiwtMTg2MTQ2NDA0XX0=
-->