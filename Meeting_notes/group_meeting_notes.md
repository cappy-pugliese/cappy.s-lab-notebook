# Lab meeting Notes

## 09-26-25

-   talked about Andrius's ERC paper
-   For next lab meeting: read through paper - what's missing? - anything that needs clarification or needs to be explained?
-   project updates in about 2 weeks

------------------------------------------------------------------------

## 10-03-25

https://clauswilke.com/dataviz/ - look more into the geospacial data - choropleth mapping --\> - code for all the figures (and everything else) are on github

-   figure design
    -   cow plot: adds some defaults to ggplot
    -   colorblindness website simulator
        -   okabe ito: color scale
        -   viridis scale --\> not super friendly for ink when printing
        -   wesanderson R color packages
            -   zeesoo color similar to viridis
    -   one of the first things to define when creating figures in R: color pallete (keep them all the same)
        -   `theme_set(theme_cowplot())`
        -   make variable with colors
    -   don't include inconvieniet aspects of the data
        -   don't overload figures with too much information
        -   what are you trying to show with your figure?
    -   double coding
        -   put in multiple ways (i.e. both color and shapes) to view the same info
    -   be careful with scaling on figures (esp for FST)
    -   log scaling
        -   if data point = zero, has trouble plotting
            -   sudo log scaling
            -   add very low value to all points
        -   taking the square root --\> works similar to logrithmic scale
            -   careful with labeling to not confuse (go 2,4,9,16,etc)
-   climate change data:
    -   climate spiral
        -   technically correct
        -   good visualization
        -   does make the temp change seem more drastic

------------------------------------------------------------------------

## 10-17-25

-   I presented a powerpoint on where I'm at with my research

-   read 4,5,6 & ch15 in the displaying data book

    -   ignore cartograms, skip projections

    -   look at code for graphs on the github

------------------------------------------------------------------------

## 10-24-25

-   colorblindr package for R –\> lets you test your figure with various colorblindnesses

-   mapping data

    -   sf package for R

    -   ggmap

        -   geom points will plot in lat long on the map

    -   world clim

        -   seconds –\> how far apart their data points are (30 secs = lot more data)

    -   getting the map

        -   packages

            -   maps

            -   r open street map package