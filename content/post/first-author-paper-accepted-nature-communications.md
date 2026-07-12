+++
date = '2026-07-12T19:30:26+02:00'
draft = false
pin = true
title = 'First-author paper accepted at Nature Communications'
summary = '"To join or not to join: handling biological replicates in long-read RNA sequencing data": a framework for combining multi-sample long-read RNA-seq data, benchmarked across six transcript reconstruction tools.'
tags = ['bioinformatics', 'long-read-sequencing', 'publication']
cover = '/images/activities/placeholder.svg'
+++

Our paper **"To join or not to join: handling biological replicates in long-read RNA sequencing data"** has been accepted for publication in *Nature Communications* (preprint on [bioRxiv](https://doi.org/10.64898/2025.12.09.693269), 2025).

As long-read RNA sequencing (lrRNA-seq) studies increasingly include many biological replicates, how those samples get combined during transcript reconstruction has a real impact on the resulting transcriptome, yet the trade-offs were never formally characterized. We define and benchmark two strategies:

- **Join & Call (J&C):** combine reads from all samples first, then identify transcripts.
- **Call & Join (C&J):** identify transcripts per sample first, then merge the resulting annotations.

We applied both strategies to a highly replicated mouse brain and kidney dataset (PacBio and ONT), across six widely used transcript reconstruction tools (FLAIR, IsoQuant, Bambu, TALON, Mandalorion, IsoSeq). The upshot: there's no universally better strategy. J&C tends to win for discovering rare, novel isoforms, while C&J is far more computationally efficient and often sufficient when rare-isoform discovery isn't the primary goal. The right choice depends on the tool and the research question.

As first author, I developed a nextflow pipeline to reproducibly conduct the transcript reconstruction and benchmarking analysis (FLAIR, IsoQuant, Bambu, TALON, TAMA Merge, stringtie-merge, SQANTI3) across PacBio, ONT, and Illumina platforms.
