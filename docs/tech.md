---
title: Behind the scenes
authors:
    - Julio Diaz Caballero
    - Tung Trinh
---

# Assembly pipeline

## Workflow process
The workflow consists of the following steps

1. QC reads using `FastQC` before trimming
2. Trim reads using trimmomatic (dynamic MIN_LEN based on 30% of the read length)
3. QC reads using `FastQC` after trimming
4. Check for contamination using `confindr`
5. Count number of reads and estimate genome size using `Mash`
6. Downsample reads
7. Merge reads using `Flash` where the insert size is small
8. Assemble reads using `SPAdes`
9. Assess species identification using `bactinspector`
10. Assess assembly quality using `Quast`
11. Summarise QC metrics with `QuailFyr`


## Software used within the workflow
  - [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/) A quality control tool for high throughput sequence data.
  - [Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic) A flexible read trimming tool for Illumina NGS data.
  - [Cutadapt](https://github.com/marcelm/cutadapt/) Finds and removes adapter sequences, primers, poly-A tails and other types of unwanted sequence from high-throughput sequencing reads
  - [mash](https://mash.readthedocs.io/en/latest/) Fast genome and metagenome distance estimation using MinHash.
  - [lighter](https://github.com/mourisl/Lighter) Fast and memory-efficient sequencing error corrector.
  - [seqtk](https://github.com/lh3/seqtk) A fast and lightweight tool for processing sequences in the FASTA or FASTQ format.
  - [FLASH](https://ccb.jhu.edu/software/FLASH/) (Fast Length Adjustment of SHort reads) A very fast and accurate software tool to merge paired-end reads from next-generation sequencing experiments.
  - [SPAdes](http://cab.spbu.ru/software/spades/) A genome assembly algorithm designed for single cell and multi-cells bacterial data sets.
  - [contig-tools](https://pypi.org/project/contig-tools/) A utility Python package to parse multi fasta files resulting from de novo assembly.
  - [Quast](http://quast.sourceforge.net/quast) A tool to evaluate the aulaity of genome assemblies.
  - [ConFindr](https://github.com/OLC-Bioinformatics/ConFindr) Software that can detect contamination in bacterial NGS data, both between and within species.
  - [QualiFyr](https://gitlab.com/cgps/qualifyr) Software to give an overall QC status for a sample based on multiple QC metric files
  - [MultiQC](https://multiqc.info/) Aggregate results from bioinformatics analyses across many samples into a single report
  - [KAT](https://github.com/TGAC/KAT) The K-mer Analysis Toolkit (KAT) contains a number of tools that analyse and compare K-mer spectra
  - [BactInspector](https://gitlab.com/antunderwood/bactinspector) Software using an updated refseq mash database to predict species
