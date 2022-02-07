# Automated composition of the Cascabel Pipeline

Cascabel (<https://doi.org/10.3389/fgene.2020.489357>) is a variable pipeline for amplicon sequence data analysis.

It makes an interesting use case for workflow work with bio.tools/EDAM and APE, as it already foresees several variants of the main workflow, and potentially more can be found when taking to account the full content of bio.tools.

## Notes

Takes raw data as input and delivers a table of operational taxonomic units (OTUs)
or Amplicon Sequence Variants (ASVs) in BIOM and text format and representative sequences.

- For inputs and outputs: *`type`* `(`*`comma separated formats`*`)`.
- <sup>n</sup> : Could not be found in [bio.tools](https://bio.tools), based on context from Cascabel or other source.

| **Tool** | **in bio.tools** | **ID** | **Inputs** | **Outputs** |
| -------- | ---------------- | ------ | ---------- | ----------- |
| Minimum entropy Decomposition (MED) | No | - | - | - |
| Swarm | Yes | biotools:swarm | Nucleic acid sequence (FASTA-like) | Sequence cluster (Textual format) |
| DADA2 | Yes | biotools:dada2 | Demultiplexed FASTQ files<sup>9</sup> | Sequence variants<sup>9</sup> |
| deblur | No | - | - | - |
| QIIME | Yes | biotools:qiime | Raw sequence<sup>6</sup> | - |
| QIIME 2.0 | Yes | biotools:qiime2 | Raw sequence<sup>6</sup> | - |
| mothur | No | - | Sequence<sup>13</sup> | Taxonomy summary<sup>12</sup> |
| VSEARCH | Yes | biotools:vsearch | Nucleic acid sequence | Sequence similarity score, sequence alignment |
| FastQC | Yes | biotools:fastqc | Raw sequence (FASTQ-like format (text), SAM, FASTQ, BAM) | Sequence report (HTML) |
| PEAR | Yes | biotools:pear | - | Sequence assembly<sup>5</sup> |
| Cutadapt | Yes | biotools:cutadapt | RNA sequence (FASTQ, FASTA) | RNA sequence (FASTQ, FASTA) |
| Cutadapt 1.12 | Yes | biotools:cutadapt_1.12 | RNA sequence (FASTQ, FASTA)<sup>4</sup> | RNA sequence (FASTQ, FASTA)<sup>4</sup> |
| SortMeRna | Yes | biotools:sortmerna | (FASTA, FASTQ), RNA database<sup>14</sup> | - |
| trie | No | - | - | - |
| UCLUST | No | - | Sequence (FASTA, FASTQ)<sup>2</sup> | - | - |
| UCLUST_REF | No | - | - | - |
| USEARCH | Yes | biotools:usearch | Sequence (FASTA, FASTQ)<sup>1</sup> | (FASTA, FASTQ)<sup>1</sup> |
| USEARCH_REF | No | - | - | - |
| CD-HIT | Yes | biotools:cd-hit | Sequence alignment (FASTA) | Data (Textual format), Data (Textual format), Sequence alignment (FASTA) |
| SUMACLUST | No | - | Sequence<sup>3</sup> | - |
| BLAST | No | - | Sequence<sup>15</sup> | Statistical estimate score<sup>15</sup> |
| BLAST+ | No | - | Sequence<sup>15</sup> | Statistical estimate score<sup>15</sup> |
| pynast | No | - | - | - |
| MAFFT | Yes | biotools:MAFFT | Sequence (FASTA) | Sequence alignment (FASTA) |
| Infernal | Yes | biotools:infernal | Sequence profile (Sequence profile format) | Database search results |
| ClustalW (BioLib) | Yes | biotools:clustalw_biolib | Sequence (FASTA) | Sequence alignment (ClustalW format, FASTA, nexus-seqm, PHYLIP format) |
| ClustalW (PBIL) | Yes | biotools:clustalw_pbil | Sequence (FASTA) | Sequence alignment (FASTA) |
| ClustalW (SIB) | No | - | Sequence (FASTA) | Sequence alignment (FASTA) |
| RAxML | Yes | biotools:raxml | Phylogenetic tree<sup>8</sup> | - |
| FastTree | Yes | biotools:fasttree | - | Phylogenetic tree<sup>7</sup> |
| Krona | Yes | biotools:krona | (XML, Textual format)<sup>11</sup> | (HTML)<sup>10</sup> |

1. [drive5.com](http://www.drive5.com/usearch/manual/cmdline.html)
2. [drive5.com](https://www.drive5.com/usearch/manual/uclust_algo.html)
3. [Sumaclust Wiki](https://git.metabarcoding.org/obitools/sumaclust/wikis/home)
4. Does not have inputs and outputs in bio.tools. Is based on other Cutadapt.
   **Note**: according to bio.tools, Cutadapt is a "Sequence trimming" operation while Cutadapt 1.12 "Data handling". "Sequence trimming" being [more specific](https://edamontology.github.io/edam-browser/#operation_3192).
5. Based on [PEAR documentation](https://cme.h-its.org/exelixis/web/software/pear/doc.html).
6. Based on [QIIME's description on bio.tools](https://bio.tools/qiime).
7. Based on [FastTree's description on bio.tools](https://bio.tools/fasttree).
8. Based on [FastTree manual](https://cme.h-its.org/exelixis/resource/download/NewManual.pdf).
9. Based on [DADA2's description on bio.tools](https://bio.tools/dada2).
10. Based on [Krona's description on bio.tools](https://bio.tools/krona).
11. Based on [Krona's wiki on GitHub](https://github.com/marbl/Krona/wiki/Help).
12. Based on [mothur_krona's description on bio.tools](https://bio.tools/mothul_krona).
13. As described by [mothur's manual](http://mothur.org/wiki/mothur_manual/).
14. As described by [SortMeRna's website](https://bioinfo.lifl.fr/sortmerna/sortmerna.php).
15. As described by [BLAST's website](https://blast.ncbi.nlm.nih.gov/Blast.cgi).
