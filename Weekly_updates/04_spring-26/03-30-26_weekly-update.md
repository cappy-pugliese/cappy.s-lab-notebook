## This week 3/30 - 4/03
### focus on:
- [x] powerpoint
    - [x] presenting on tuesday to lab
- [x] start making phylogenies?
- [] writing

### Monday (3/30)
- worked on powerpoint (finishing)
    - finished
- trying to get a more accurate snp count
    - currently have the same count for all the different groups, when I know that is not true
    - remaking vcf for north american pd samples to see difference between all and north american snp count
        - put bcfview running to filter it out, next step is to count the number of snps

### Tuesday (3/31)
- presented to lab, lots of comments
    - reorder/add more to certain slides
    - fix figures (especially pixy)
    - more info on certain things
    - fix conclusion statements
    - look for bat migration patterns / locations
    - figure out how to prove genetic divergence
    - pca plot for clades
    - [x]fix feems color scheme??
- fixed feems visibility issue
    - did not change the color scheme (so things would still match), but graphed it in R and gave a more contrasting background/added outline
    - updated powerpoint with new graph

### Wednesday (4/1)
- made progress with defense scheduling
    - sent email to advisory committe about timing
    - sent email to harrison about booking rooms
- [x] put iqtree running

### Friday (4/3)
- fixed plink script to generate a haploid .phy file
- reran iqtree (a few times)
    - once with the same dataset, and once with only pd
    - turns out the Pd_70 sample is actually one of the asian samples, not part of either of the European clades
- backed up scripts on github

- want to work on writing next week, because I'm stressing about it
- I fear if I keep running more and more things, I'm never going to get the writing portion done

## Week 4/6 - 4/10

### Monday (4/6)
- did not meet for individual lab meeting
- worked on making some better graphs for pixy to see the differences in years better
- tried to work on writing, ended up reading a bunch of papers and going down a research rabbit hole that led me nowhere
- read lab meeting paper

### Wednesday (4/8)
- spent lot of time working on introduction
- I may or may not be making the introduction too long
- added some more sources in zotero (included in introduction)

### Friday (4/10)
- edited names on phylogeny
- ran a new iqtree group
- edited names on new phylogeny
- color coded the new phylogeny by year

## Week 4/13 - 4/17
todos
- focus on writing!!!

### Monday (4/13)
- basically finished intro
- added figures to paper

### Tuesday (4/14)
- **need to (try to) finish writing and send in to lab by Sunday**
    - **try to send to advisory committee by next week**
- worked on writing results section
- edited figure 1 so the pca percentages are present

### Wednesday (4/15)
- Working on writing results section
    - got sidetracked and am rerunning the phylogeny because I want to use regular bootstrapping instead of ultrafast bootstrapping
    - put runs going for only_pd and n-amer_pd groups
    - runs finished, still need to look at, but I am able to see the different trees now which is what I wanted
- wrote like ~2 paragraphs in the results section
    - would have done more, but had to drive home today

### Thursday (4/16)
- worked on writing results
- changed phylogeny for figure 1 with the regular bootstrapping run

### Friday (4/17)
- working on results section
    - population structure portion is nearly complete
        - [] need to make figure 2 for north american phylogeny / pca?? results
            - could honestly probably put the pca results in supplemental, might just be beating a dead horse at this point if I keep it in the actual paper.
        - [] add on to results from figure 3
        - [] probably need to go back and edit all the figure legends
    - working on pixy portion

paper todos:
- [] last sentence in intro
- [] finish the methods section
- [] finish results
- [] write discussion
- [] write conclusion
- [] add in all the missing citations and reorganize
- [] get rid of any unused citations
- [] add figures/tables to supplemental portion

### Saturday (4/18)
- added more to results
- added a little to methods
- added in comments on what I have left to do
- tried to get better pixy calculations, but pixy decided not to work on me
    - trying to troubleshoot a lil
- remade algatr tess figure

- [] check on pixy runs on xanadu
    - if both of them have issues:
        - try running another old run (or two) on mantis
        - send an issue in on github
        - seems like it might be an issue with the code itself, but I don't know why it worked back in march but is not longer working now??? something is funky.

### Sunday (4/19)
- did some more writing
    - finished the FEEMS section
    - edited/added to methods
    - edited things here and there
- xanadu runs
    - the older one ran just fine, the newer one still ran into problems
    - giving up on it at this point, it's not worth the trouble with the amount of time I have left
- edited north america phylogeny and made new pca plots
    - still debating how to format/which pca plots to use

### Monday (4/20)
- made figure for North American phylogeny + PCAs
- reran FEEMSmiz with k = 7 instead of 10
- added on to thesis/edited
- ran a new phylogeny with all samples (including all outgroups)
    - realized my original run with the outgroup only included one european and one asian sample
    - ran with more than one outgroup just in case
    - some of the north american samples branch out before the european and asian samples
        - running again with actual bootstrapping
        - wondering if there was recombination happening between fungal Pseudogymnoascus species
        - would be interesting if that is the case
        - obviously that might be too much to add on right now, but would be very interesting