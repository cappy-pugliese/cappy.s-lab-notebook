# Weekly Update: 5/7 - _insert date_

## defense comment todos
[] fixing phylogenies, talking with Elizabeth
[x] gdm with genetic distance vs geographic vs time
[] add section in results about time and space being confounding
    [] address what is not confounded
[] structure thesis similar to powerpoint, add in research questions
    [] cite why you have those expectations/questions
[] Be careful with general use of terms

## focus for rest of the week 5/7 - 5/11
[x] work on defense comments
[x] algatr gdm with time instead of environmental data

## Thursday (5/7)
- focused on algatr gdm
    - step 1: get genetic distance by time pc
    - originally got an error when trying to make the pca, and spent a few hours doing nonsense only to realize why it didn't work in the first place
    - made the time pca
    - was able to run about half of the gdm vignette
        - the raster part was giving me trouble
        - could not find any useful help from the internet
        - eventually gave up on generating the map
- found that time has a much stronger predictor importance compared to geographic distance (with significance of p = 0.03)

## Friday (5/8)
- had to run errands so didn't get much done
- Andrius sent code for matrix regression
    - code did not quite work, was able to make a different time_dist matrix by cheating and using the ALGATR gen_dist() function
    - all predictors were statistically significant (genetic distance, geographic distance, and time)
- need to check in with Dan about code accuracy
    - [] try to see if I can talk with him on monday? or send an email

## Sat/Sun
- [] figure out what model works best with data
    - attempted, but kept running into iqtree errors
    - might need to use an earlier version of iqtree
        - xanadu has earlier versions --> might need to run there
- [x] maybe try running with all sites instead of snps
    - allsites does not work when making phylip file for iqtree
    - phylip file only takes snps

## Monday
- [x] meet with Elizabeth to talk about phylogenies
    - try filtering vcf again, this time with different filtering parameters
        - original vcf
        - set m to 1 and M to 4
        - include invariant sites in the model (+I)
        - run ultrafast, make sure it is ran with + nni (should do automatically, but double check)
- filtered out vcfs
    - tried running the new filtered vcfs with plink to generate phylip files and it didn't work
    - I think plink needs biallelic data to generate the phylip file
- I'm going to take a break but when I come back:
    - [] redo vcfs but with it set back to m2 and m4
    - if it's still broken then it's something else going wrong (doubt it, but you never know)
    - [] run plink
    - [] run iqtree