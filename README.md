# Cappy's Lab Notebook

This is my lab notebook for the Dagilis lab 💻🦇🍄

Click [here](/Weekly_updates) to see my lab notebook entries

------------------------------------------------------------------------

## Project Progress Summaries

### 2024 Fall Semester

#### WNS Background

-   read papers to learn more about WNS
-   looked at <https://www.whitenosesyndrome.org/>

#### Learned how to use github

-   started making these weekly updates and pushing commits to github
-   also made my own website (took a while) using github and edited info on the lab website

#### Learned how to use the cluster

-   learned how to navigate around my computer on the terminal
-   watched xanadu intro videos
-   learned how to log into the cluster
-   got familiar with bash
-   learned how to make directories and edit files among other things

#### Learned about NCBI and Quality checking

-   got used to finding samples on NCBI
-   learned about fastqc and how to interpret the output html file
    -   also had to learn how to transfer files from the cluster to my laptop

#### Followed Dagilis's WNS tutorial

-   short-read sample analysis pipeline using one sample to start with
-   learned how to download sample from NCBI onto the cluster (fastq-dump)
-   learned how to trim sequences (bbduk)
-   learned how to align to reference
    -   created sam/bam files using bwa-mem, picard, samtools
-   variant calling with mpileup and GATK pipeline

------------------------------------------------------------------------

### 2025 Spring Semester

#### Courses

-   took EEB 5300: Practical Genomics
    -   learned *a lot* about bioinformatics methods that relate to my project
    -   learned how to write and submit scripts on the cluster (and got a lot of practice)
    -   got a lot of practice with trouble shooting

#### Research Committee

-   made research committee
-   had our first meeting at the end of the semester
    -   practiced presenting my project a couple of times during lab meeting and during my research committee meeting
    -   reread landscaping genomics methods papers to better understand what I plan on doing

#### Scripts

-   made some scripts to start off the pipeline from where Andrius left off
    -   indexed bam files with samtools
    -   generated g.vcfs with haplotypecaller
    -   working on finishing the GATK pipeline
-   downloaded some climatic data
-   added in some missing lat long location data
    -   still need to work on adding in the rest

------------------------------------------------------------------------

### 2025 Fall Semester

#### Courses

-   Took Popgen with Andrius and learned a lot about different analysis methods
-   Popgen lab was very helpful with making progress for my master's project

#### Making Progress

-   made my master's plan of study
-   finished gathering the lat and long for the Pd locations
    -   some of the locations were *very* approximate
-   discovered that a few of the Pd samples are actually close relatives and not actually Pd while looking at the metadata
-   started annotating the sources I used to find the metadata using zotero

#### Scripts

-   finished the g.vcf pathway and got the vcf file
-   did some vcf filtering
-   ran some QC and stats analysis on the vcfs
-   ran plink and then PCAngsd
    -   originally had a bit of trouble getting PCAngsd to work on the cluster, but I eventually figured it out
    -   had to figure out how conda environments worked
    -   ran them again for different groupings of my Pd samples
        -   i.e. one excluding the non Pd samples, and one only including the North American Pd samples
-   made a bunch of PCAngsd graphs
-   worked on scripts for iqtree
    -   still have yet to finish running those
    -   ran into issues -- turned out to be something wrong with the version of iqtree 3.0 itself