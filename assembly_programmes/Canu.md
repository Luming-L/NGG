Genomic repeats longer than read length will disturb overlapping of reads. Single-molecule sequencing can produce reads > 10kb, but it is less accurate.

PacBio single-molecule real-time (SMRT) and Oxford Nanopore strand sequencing have their own characters and requirements for assembly. 

New approaches come out to deal with data with increased read length and error rate. These can be roughly categorised as hybrid, hierarchical or direct methods.

Hybrid methods rely on complementary short reads for accurate base calls.
Hierarchical methods use multiple rounds of read  overlapping (alignment) and correction to improve read quality prior to assembly.
Direct methods attempt to assemble from a single overlapping step without any prior correction.

Here focus on HM, because it has produced the most continuous de novo assemblies to date.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY4Mzk5MjE0NiwtMzA4MzExXX0=
-->