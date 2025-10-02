---
title: About
authors:
    - Julio Diaz Caballero
    - Tung Trinh
---

# About the SeQUencIng and antimicrobial Resistance epidemiology Linkage (SQUIRL) : A simple desktop application for genome assembly of short and long read data

The team at the [Centre for Genomic Pathogen Surveillance](https://www.pathogensurveillance.net) and [Oxford University Clinical Research Unit - Hanoi](https://www.oucru.org/location/oucru-ha-noi/) has designed this application to offer a user-friendly genome assembly workflow. This process includes implementing quality control measures on the raw sequencing data to optimize it for assembly. Subsequently, the application utilizes the [`Spades`](https://github.com/ablab/spades) assembler for `short read`, [`Flye`](https://github.com/mikolmogorov/Flye) for `long read` and [`Uniclye`](https://github.com/rrwick/Unicycler) for hybrid assemblies. The app itself also gathers quality metrics throughout the workflow. These metrics are then presented alongside the final assembly in `fasta` format.