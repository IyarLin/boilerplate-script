Novel research that will disrupt the industry
================
Mr scientist
08 May, 2021

-   [Load data](#load-data)
-   [Don’t be afraid to add headers along the
    report](#dont-be-afraid-to-add-headers-along-the-report)
    -   [They’ll all show up in the table of
        contents!](#theyll-all-show-up-in-the-table-of-contents)
-   [There’s also plots and tables all
    around](#theres-also-plots-and-tables-all-around)
-   [Another cool option is doing code
    folding](#another-cool-option-is-doing-code-folding)
-   [Rendering Latex](#rendering-latex)

<br>

# Load data

``` r
source("../passwords.R") # never post your passwords to Github again!
```

# Don’t be afraid to add headers along the report

<br>

## They’ll all show up in the table of contents!

<br>

# There’s also plots and tables all around

``` r
plot(mtcars$mpg, mtcars$cyl)
```

![](README_files/figure-gfm/show%20a%20plot-1.png)<!-- -->

``` r
pandoc.table(head(mtcars[, 1:4]))
```

|                       | mpg  | cyl | disp | hp  |
|:---------------------:|:----:|:---:|:----:|:---:|
|     **Mazda RX4**     |  21  |  6  | 160  | 110 |
|   **Mazda RX4 Wag**   |  21  |  6  | 160  | 110 |
|    **Datsun 710**     | 22.8 |  4  | 108  | 93  |
|  **Hornet 4 Drive**   | 21.4 |  6  | 258  | 110 |
| **Hornet Sportabout** | 18.7 |  8  | 360  | 175 |
|      **Valiant**      | 18.1 |  6  | 225  | 105 |

<br>

# Another cool option is doing code folding

<details>
<summary>
SOME CODE
</summary>
<p>

#### Like this!

``` r
print("source: https://gist.github.com/joyrexus/16041f2426450e73f5df9391f7f7ae5f")
```

    ## [1] "source: https://gist.github.com/joyrexus/16041f2426450e73f5df9391f7f7ae5f"

</p>
</details>

# Rendering Latex

You can render Latex on a github document by specifying in the YAML
header:

``` r
output:
  github_document:
    pandoc_args: --webtex
```

Here’s an example:

![
X \\sim \\mathcal{N}(\\mu,\\sigma^2) \\rightarrow f(x)= \\frac{1}{\\sigma \\sqrt{2\\pi}}e^{-\\frac{1}{2}\\left(\\frac{x-\\mu}{\\sigma}\\right)^2}
](https://latex.codecogs.com/png.latex?%0AX%20%5Csim%20%5Cmathcal%7BN%7D%28%5Cmu%2C%5Csigma%5E2%29%20%5Crightarrow%20f%28x%29%3D%20%5Cfrac%7B1%7D%7B%5Csigma%20%5Csqrt%7B2%5Cpi%7D%7De%5E%7B-%5Cfrac%7B1%7D%7B2%7D%5Cleft%28%5Cfrac%7Bx-%5Cmu%7D%7B%5Csigma%7D%5Cright%29%5E2%7D%0A "
X \sim \mathcal{N}(\mu,\sigma^2) \rightarrow f(x)= \frac{1}{\sigma \sqrt{2\pi}}e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}
")
