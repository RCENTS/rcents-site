---
title: Short Read Error Correction
---

<div class="starter-template" markdown="1"> 


# RCENTS : Short Read Error Correction

All high throughput sequencing systems are used for redundant high coverage sampling, whether the underlying sample constitutes copies of a single genome, transcriptome, or multiple individual organisms from multiple species (metagenome). While some coverage is needed to ensure all of the underlying target sequences are sampled, a much higher degree of coverage is employed to overcome the effects of sequencing errors, particularly when searching for variants with relatively low abundance. 

From an algorithmic perspective, both sequencing errors and biological variants appear in the form of substitutions, insertions, and deletions. As sequencing errors are random, and dependent on relative position within the read, high coverage helps distinguish sequencing errors from true biological variations. Error correction algorithms and software utilize this principle to directly identify errors in the data and correct them to improve dataset quality. An important side benefit of error correction is its effect on scalability of downstream applications. For example, erroneous reads can lead to artificially large de Bruijn graphs in the initial stage of genome assembly, thereby reducing the scale of problems that can be solved in a given memory budget. 

In this project, we evaluate the reproducibility of short read error correction software given in [software images page](images).

## Introduction
{: #lead}

For reproducibility analyses of short read error correction, we include the three main techniques used for error correction and multiple software products based on each underlying method – kmer spectrum based methods, suffix tree/array based methods, and multiple sequence alignment based methods.

The key goals of reproducibility experiments are :

1. Verify that the datasets used by the authors in their publication can be downloaded and their specification matches with respect to sequencing technology, source genome and the number of reads.
2. Verify that the software can be downloaded and run without any erraneous results with the prescribed parameters. If the source code of the software is available, verify that the source code can be compiled and their dependencies can be satisfied.
3. Verify that the output produced by the error correction software satisfy the quality requirements specifed by the authors using evaluation measure described in the respective publication. 

If ethier the software or the source code is not available for download without sending an email to the authors, we do not include in our evaluation.

## Steps in Reproducibility

For a given short read error correction software, we first select the datasets and the run parameters used by the authors in the corresponding publications. We select only those datasets which either publicly available in NCBI [Short Read Archive (SRA)](https://www.ncbi.nlm.nih.gov/sra) or can be downloaded freely without a sign-up procedure. Since none of the error correction software take into account the paired-end information, for a paired end dataset, we append the contents the _fastq_ file containing the second of the paired sequences to the _fastq_ file containing the first of the paried sequences.

In order to make sure that our reproducibility experiments can be reproducible, we make use of [docker](https://www.docker.com/) to construct software images that include all the dependencies of the respective software. With the recent intorduction of many workflow definition languages to streamline bioinformatics workflows, we use [nextflow](https://www.nextflow.io) scripts to describe all the steps in our experiments. Whenever possible, we use the same tools authored by the publication authors to evaluate the error correction results.

A reproducibility experiment consists of the following steps:
 
1. From the publication, select the datasets, run parameters and the evaluation metric. 
2. Construct a docker image of the error correction software.
3. Develop a [nextflow](https://www.nextflow.io) script of all the steps of reproducibility.
4. If authors didn't provide scripts for evaluation metrics, develop a script to evaluate the error correction tool as specified in the publication.
5. Run the experiments and document the evaluation.


Links to all images can be accessed from our [Software Images](images) page and all the nextflow scripts are available in our [RCENTS](http://github.com/rcents/ec/) github repository. Results of the reproducibility experiments are available in the [Reproducibility](repro) page.

<!--
## Summary

 1. How much sucess
2. What are the difficulties
3. Where can a user find the details
-->

</div>
