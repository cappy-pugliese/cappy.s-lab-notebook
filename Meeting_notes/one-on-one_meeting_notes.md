# One on one meeting notes

## 09-15-25

-   run vcfr / qc analysis on vcf file

```         
-i "MAF > 0.1"
# or
-i "QUAL > 10" ## <- phred score (or 20, probs better) ##
```

-   filtering depends on file --\> need qc step - allele freq bins (bcftools stats)

-   pcangst for population structure run pixy

-   look at heterozygocity

------------------------------------------------------------------------

## 09-22-25

-   filter out indiv and sites

-   filter out low depth (i.e. 8 is kinda low depth)

-   common ways to filter:

    -   SNPS (-v snps)

    -   -m2 (minimum alleles with 2) –\> biallelic wont work with pixy

    -   QUAL \> 20

    -   greater than 4 or 5 for depth

        -   `-i QUAL > 20 && DP > 5`

        -   start with relatively low filtering when looking at the data

chmod 770 \[file/directory\] –\> will grant permissions to Andrius as well (anyone with folder permissions has access)

-   label samples for latitude & longitude
-   PCA analysis in R
-   PCAngsd, will need beagle or plink formated files
    -   plink is much faster converting things
        -   make -bed
        -   only use the haploid data for this

------------------------------------------------------------------------

## 09-29-25

-   try and get some data out
-   cluster gets busier towards the end of the semester
-   results so far are showing genetic variability

before thursday: - send pca plot or some ancestry file that it produces

------------------------------------------------------------------------

## 10-06-25

-   make bin and add to paths

-   will need to source .bashrc for scripts

-   destructans data

    -   population structure (pcangsd)

        -   if there is population structure –\> can run fiends(?) (FEEMS???)

        -   smc++ for demographics

-   no class at all this week

------------------------------------------------------------------------

## 10-14-25

-   [x] rerun pcangsd with admix option

-   run pixy without Fst

-   meet thurs after lab

-   focus on getting lat and long of all the individs

-   [x] run ld pruned at some point --\> plink's ld pruning

    -   specific option, `indep-pairwise`

    -   default: 10kb step size: 500/1,000

    -   r\^2 threashold, anything above .5

    -   https://www.cog-genomics.org/plink/1.9/ld

different packages:

-   aligtr

    -   pipeline focused on conservation

    -   but want to know similar things

    -   need to add in specific coordinates

for friday compare what we find to what the other papers found

-   future directions:

    -   run phylogeny analyses - iqtree

        -   split into smaller windows

        -   into astral to calculate species tree

    -   LDK analysis

    -   plink calculations

    -   pixy

        -   pi, fst

        -   maybe some selection stuff

-   plan for committee meeting in spring

------------------------------------------------------------------------

## 10-20-25

-   metadata table

    -   sample_id, SRA, source, location (Country, state, lat, long), major ancestry (\>50%) from pcangsd

    -   major ancestry

        -   apply(matrix, 1, funciton(x) –\> which (x\>0.5) )

-   iqtree

    -   need to download refseq data from ref genome

    -   dont run something on under 100kb chromosomes

    -   sent scripts over slack

        -   one of the scripts is wonky

            -   windows too big? –\> needs to run on at least two windows, but some of the scaffolds are too small)

            -   use updated version of script –\> edited it in slack

                -   dont forget to module load iqtree3

        -   change scripts to work with newer version of iqtree

        -   can change around slurm parameters

        -   make sure output directory exists

        -   might need to index vcf (if there's a .tbi then i'm fine)

    -   vcf filters

        -   biallelic snps

        -   -m2

        -   -M2

        -   -v 'snps'

        -   -i 'MAF\>0.05'

        -   -i'GQ\>20'

    -   plink did filter vcf, but does not output an actual vcf

        -   maybe redo plink & pcangsd on same filtered vcf that I will be using for iqtree

    -   will eventually use astral4 (ASTER)

        -   overall estimator of phylogenetic tree

        -   has an actual console can use to look at trees

            -   will eventually need to concatinate all of the files astral4 generates

            -   and use that file to generate trees

------------------------------------------------------------------------

## 10-23-25

-   will need to use plink 2 with the scripts (will need to download plink 2)

-   window use 10kb

## 10-27-25

--mimd

-   need about 25%, so things don't mess up down the line

-   for plink 2

## 11-03-25

-   can use ggtree to visualize trees in R

    -   <https://yulab-smu.top/treedata-book/chapter7.html>

-   FEEMS –\> all built in python

-   ALGATR –\> all built in R, needs lat long data

## 11-11-25

for iqtree issue

-   try running on bigger windows

-   checkpoint time –\> set it to an hour if checkpoints are breaking

-   keep redo flags –\> don't start from a checkpoint

-   might be file write issues

-   try whole genome analysis

    -   plink make a whole chromosome

    -   maybe not the greatest method

11-17-25

-   need to defend before like may 15?

-   start of may possibly

-   to include in paper

    -   pca

    -   structure

    -   pi across the genome

        -   and for each ancestry

        -   try running with pixy

        -   or piawka (runs on vcf directly)

        -   or some R package (i.e. popgenme)

    -   differentiation between populations

        -   dxy and Fst

        -   same package as pi

    -   dN/ds –\> will need an outgroup

        -   run with PAML

    -   trees

        -   iqtree and ASTRAL-IV

    -   need lat longs

        -   FEEMS

            -   will likely take a while

            -   need to use python

        -   tess

            -   will be in source code for class 11/18

        -   aligatr