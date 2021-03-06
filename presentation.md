# Assembly of large genome

# The axolotl genome and the evolution of key tissue formation regulators

## Part 1: the axolotl genome
### A long-read assembler for large genomes
d/d axolotl strain (mutant)
It is easy to acquire live imaging so it is used in laboratory regeneration studies. We sequence the genome of axolotl.
The genome is large and complex (32 Gb).
We sequence the genome: 110 million long reads, 32x **coverage**, **N50** read length 14.2kb, **PacBio**.
avoid sample bias, span long repeat region (double check: one long read spanning, some smaller reads truly overlapping the long read)
An assembly algorithm: MARVEL
MARVEL has two-phase read-correction to keep PacBio reads intact for assembly.
MARVEL produced a **contig assembly** with an N50 of 218kb.
7x illumina-based sequencing to correct sequence errors in 1% of contig base
**heterozygosity**
genome sequencing strategy:
pacbio sequencing to get long reads - contig assembly with MARVEL - 7x illumina sequencing to get short reads for correction with **Pilon** - **optical map** to **scaffold** and correct **chimeric contigs** (**slightly reduce N50 contig length to 216kb**, final **hybrid assembly** **N50 scaffold** length 3Mb)
The assembly of axolotl genome is good, because 98.5% UCEs (non-exonic ultraconserved elements) across vertebrates align to axolotl assembly.
to further assess the completeness of the assembly, generate a gene catalogue by sequencing mRNA from 22 tissues.
All 180649 transcript contigs contained 99% conserved core eukaryotic genes.
### Expansion of long terminal repeat retroelement
similar number of genes in other smaller vertebrate genomes
repetitive sequences made up 65.6% of the contig assembly
most repetitive sequences are **LTR (long terminal repeat) **
Most LTR are **endogenous retroviruses**
Some elements are more than 10kb in length.
97% of contigs ended in LTR elements 
The number of substitution to the repeat consensus - an estimate of the relative age of the LTR retroelement **no. subs per site** - the axolotl genome has undergone a long period of transposon activity
median intron size expands.
### HoxA cluster and intron size constraints
HoxA locus is important in proximal-to-distal limb development and is reactivated during limb regeneration.
HoxA is a cluster having a bunch of genes?
each gene has two exons and an intron.
HoxA in axolotl has a increased repeat content and is 3.5 times larger.
highly conserved non-exonic elements are not interspersed in the 170-kb repetitive region between HoxA3 and HoxA4
the expansion of introns of developmental genes is significantly lower (6- to 11-fold, P<10-11)
introns of developmental genes in axolotl are shorter than introns of non-developmental genes

## Part 2: the evolution of key tissue formation and regulators
### A reduced Pax-family complement
the genome for families of canonical developmental signalling molecules
### Axolotl Pax7 has similar functions to Pax3
### Species-restricted genes in regeneration


# Synchronization

Synchronization is one of the biggest features of StackEdit. It enables you to synchronize any file in your workspace with other files stored in your **Google Drive**, your **Dropbox** and your **GitHub** accounts. This allows you to keep writing on other devices, collaborate with people you share the file with, integrate easily into your workflow... The synchronization mechanism takes place every minute in the background, downloading, merging, and uploading file modifications.

There are two types of synchronization and they can complement each other:

- The workspace synchronization will sync all your files, folders and settings automatically. This will allow you to fetch your workspace on any other device.
	> To start syncing your workspace, just sign in with Google in the menu.

- The file synchronization will keep one file of the workspace synced with one or multiple files in **Google Drive**, **Dropbox** or **GitHub**.
	> Before starting to sync files, you must link an account in the **Synchronize** sub-menu.

## Open a file

You can open a file from **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Open from**. Once opened in the workspace, any modification in the file will be automatically synced.

## Save a file

You can save any file of the workspace to **Google Drive**, **Dropbox** or **GitHub** by opening the **Synchronize** sub-menu and clicking **Save on**. Even if a file in the workspace is already synced, you can save it to another location. StackEdit can sync one file with multiple locations and accounts.

## Synchronize a file

Once your file is linked to a synchronized location, StackEdit will periodically synchronize it by downloading/uploading any modification. A merge will be performed if necessary and conflicts will be resolved.

If you just have modified your file and you want to force syncing, click the **Synchronize now** button in the navigation bar.

> **Note:** The **Synchronize now** button is disabled if you have no file to synchronize.

## Manage file synchronization

Since one file can be synced with multiple locations, you can list and manage synchronized locations by clicking **File synchronization** in the **Synchronize** sub-menu. This allows you to list and remove synchronized locations that are linked to your file.


# Publication

Publishing in StackEdit makes it simple for you to publish online your files. Once you're happy with a file, you can publish it to different hosting platforms like **Blogger**, **Dropbox**, **Gist**, **GitHub**, **Google Drive**, **WordPress** and **Zendesk**. With [Handlebars templates](http://handlebarsjs.com/), you have full control over what you export.

> Before starting to publish, you must link an account in the **Publish** sub-menu.

## Publish a File

You can publish your file by opening the **Publish** sub-menu and by clicking **Publish to**. For some locations, you can choose between the following formats:

- Markdown: publish the Markdown text on a website that can interpret it (**GitHub** for instance),
- HTML: publish the file converted to HTML via a Handlebars template (on a blog for example).

## Update a publication

After publishing, StackEdit keeps your file linked to that publication which makes it easy for you to re-publish it. Once you have modified your file and you want to update your publication, click on the **Publish now** button in the navigation bar.

> **Note:** The **Publish now** button is disabled if your file has not been published yet.

## Manage file publication

Since one file can be published to multiple locations, you can list and manage publish locations by clicking **File publication** in the **Publish** sub-menu. This allows you to list and remove publication locations that are linked to your file.


# Markdown extensions

StackEdit extends the standard Markdown syntax by adding extra **Markdown extensions**, providing you with some nice features.

> **ProTip:** You can disable any **Markdown extension** in the **File properties** dialog.


## SmartyPants

SmartyPants converts ASCII punctuation characters into "smart" typographic punctuation HTML entities. For example:

|                |ASCII                          |HTML                         |
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|


## KaTeX

You can render LaTeX mathematical expressions using [KaTeX](https://khan.github.io/KaTeX/):

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
\Gamma(z) = \int_0^\infty t^{z-1}e^{-t}dt\,.
$$

> You can find more information about **LaTeX** mathematical expressions [here](http://meta.math.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).


## UML diagrams

You can render UML diagrams using [Mermaid](https://mermaidjs.github.io/). For example, this will produce a sequence diagram:

```mermaid
sequenceDiagram
Alice ->> Bob: Hello Bob, how are you?
Bob-->>John: How about you John?
Bob--x Alice: I am good thanks!
Bob-x John: I am good thanks!
Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

Bob-->Alice: Checking with John...
Alice->John: Yes... John, how are you?
```

And this will produce a flow chart:

```mermaid
graph LR
A[Square Rect] -- Link text --> B((Circle))
A --> C(Round Rect)
B --> D{Rhombus}
C --> D
```

MARVEL assembly pipeline
To reduce both computational time and storage space
- setup phase
	- extract reads from raw data
	- save reads in a database, and split the database into blocks 
- patch phase
	- overlap by block-against-block alignment 
	- detect and correct reads artifacts (patch reads)
		- untrimmed adapters
		- polymerase strand jumps
		- ligation chimeras 
not all-against-all alignment but a block-against-block alignment
- assembly phase
	- stitch phase short alignment artifacts
	- overlap with patched reads (mask repeats)
	- annotate repeat
	- generate overlap graph
	- tour overlap graph and generate final contigs 

### Read patching
not correct reads
repairs large-scale errors
#### Broken alignment - not spanned by any alignment
In this region of the long read, the quality is quite low.
As a result, the sequence in this region of th long read is not consistent with any reads. All the alignments to this long reads break here. 
We look at the length of gaps in all alignments. If they are roughly identical, the fragment of one of the B reads can be extract to patch A.

Another picture discribes a similar scenario.
Here, we look at B1 and B2 from the perspective of A, so there are mismatchs in B1 and B2.
Here, we look at A from the perspective of B1 and B2, respectively, so there are mismatch in A.
#### Noisy regions - low quality
The sequence is bad, but not bad enough to break all alignments. 
We replace the low-quality region with B read spanning it.

The alignment can continue at the native error rate.
The longer the read, the more likely it encounter errors.
Long reads are very valuable and we should preserve them.
figure7

### Repeat masking during overlapping phase
masking server
- analyse alignments computed by overlapper jobs
- collect coverage statistics
(significant deviations from average coverage flagged as repeats)
- annotate them as repeat
- soft mask the repeat
- exclude them from k-mer seeding
save compute time and storage requirements up to one order of magnitude
- repeat-induced alignments is removed and will not be used to assembly
- disambiguate junctions in the assembly graph
```mermaid
graph LR
A[multiple millions of CPU hours/>2PB storage/one Daligner run] -- use dynamic repeat masking server --> B[150,000 CPU hours/120Tb storage space/the complete pipeline]
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQ5NDE5NzQyOSwxODE2NjMxMDQsLTIwOT
QwMTg5MTMsLTE0MDkyNDk4OTIsNTY1MjM5NTk5LC0xOTYwNzYw
NTg1LC04NTQxODIxODMsLTM4MTY2ODU4MSwtMTYxMjY5NDg5MS
wtMTE5NzYxMDUzNywtMTc5MTU3NTUyNCwxMzcxOTg1MzUzLC0x
MzM5MTg2MDc4LDE3OTM0Mzg3MzMsLTU0MjI3NjcxMCwtMTYwNj
A4ODY3NCwtMTI3MDc4MjU2NiwtMTU0MTUzMjE4OCwtMTYzMzI5
OTEwNiwtMTc2NTkzMjQ4OF19
-->