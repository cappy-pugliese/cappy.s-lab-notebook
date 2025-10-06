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

        -   if there is population structure –\> can run fiends(?)

        -   smc++ for demographics

-   no class at all this week