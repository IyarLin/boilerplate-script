Novel research that will disrupt the industry
================
Mr scientist
30 December, 2018

-   [Load data](#load-data)
-   [Don't be afraid to add headers along the report](#dont-be-afraid-to-add-headers-along-the-report)
    -   [They'll all show up in the table of contents!](#theyll-all-show-up-in-the-table-of-contents)
-   [There's also plots and tables all around](#theres-also-plots-and-tables-all-around)

Load data
=========

``` r
source("../passwords.R") # never post your passwords to Github again!
```

Don't be afraid to add headers along the report
===============================================

They'll all show up in the table of contents!
---------------------------------------------

There's also plots and tables all around
========================================

``` r
plot(mtcars$mpg, mtcars$cyl)
```

![](Boilerplate_script_files/figure-markdown_github/show%20a%20plot-1.png)

``` r
pandoc.table(head(mtcars[, 1:4]))
```

    ## 
    ## -------------------------------------------------
    ##         &nbsp;           mpg    cyl   disp   hp  
    ## ----------------------- ------ ----- ------ -----
    ##      **Mazda RX4**        21     6    160    110 
    ## 
    ##    **Mazda RX4 Wag**      21     6    160    110 
    ## 
    ##     **Datsun 710**       22.8    4    108    93  
    ## 
    ##   **Hornet 4 Drive**     21.4    6    258    110 
    ## 
    ##  **Hornet Sportabout**   18.7    8    360    175 
    ## 
    ##       **Valiant**        18.1    6    225    105 
    ## -------------------------------------------------
