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

<table style="width:71%;">
<colgroup>
<col width="33%" />
<col width="9%" />
<col width="8%" />
<col width="9%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">mpg</th>
<th align="center">cyl</th>
<th align="center">disp</th>
<th align="center">hp</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>Mazda RX4</strong></td>
<td align="center">21</td>
<td align="center">6</td>
<td align="center">160</td>
<td align="center">110</td>
</tr>
<tr class="even">
<td align="center"><strong>Mazda RX4 Wag</strong></td>
<td align="center">21</td>
<td align="center">6</td>
<td align="center">160</td>
<td align="center">110</td>
</tr>
<tr class="odd">
<td align="center"><strong>Datsun 710</strong></td>
<td align="center">22.8</td>
<td align="center">4</td>
<td align="center">108</td>
<td align="center">93</td>
</tr>
<tr class="even">
<td align="center"><strong>Hornet 4 Drive</strong></td>
<td align="center">21.4</td>
<td align="center">6</td>
<td align="center">258</td>
<td align="center">110</td>
</tr>
<tr class="odd">
<td align="center"><strong>Hornet Sportabout</strong></td>
<td align="center">18.7</td>
<td align="center">8</td>
<td align="center">360</td>
<td align="center">175</td>
</tr>
<tr class="even">
<td align="center"><strong>Valiant</strong></td>
<td align="center">18.1</td>
<td align="center">6</td>
<td align="center">225</td>
<td align="center">105</td>
</tr>
</tbody>
</table>
