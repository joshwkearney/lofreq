---
layout: default
title: Home
---


# Introduction #

LoFreq* (i.e. LoFreq version 2) is a fast
and sensitive variant-caller for inferring SNVs and indels from
next-generation sequencing data. It makes full use of base-call
qualities and other sources of errors inherent in sequencing
 (e.g. mapping or base/indel alignment uncertainty),
which are usually ignored by other methods or only used for filtering.

LoFreq* can run on almost any type of aligned sequencing data
(e.g. Illumina, IonTorrent or Pacbio) since no machine- or
sequencing-technology dependent thresholds are used. It automatically
adapts to changes in coverage and sequencing quality and can therefore
be applied to a variety of data-sets
e.g. viral/quasispecies, bacterial, metagenomics or
somatic data.

LoFreq* is very sensitive; most notably, it is able to predict
variants below the average base-call quality (i.e. sequencing error
rate). Each variant call is assigned a p-value which allows for
rigorous false positive control. Even though it uses no approximations
or heuristics, it is very efficient due to several runtime
optimizations and also provides a (pseudo-)parallel implementation.
LoFreq* is generic and fast enough to be applied to high-coverage data
and large genomes. On a single processor it takes a minute to analyze
Dengue genome sequencing data with nearly 4000X coverage, roughly one
hour to call SNVs on a 600X coverage *E.coli* genome and also roughly
an hour to run on a 100X coverage human exome dataset.

For more details on the original version of LoFreq see
[Wilm *et al.* (2012)](http://www.ncbi.nlm.nih.gov/pubmed/23066108).
