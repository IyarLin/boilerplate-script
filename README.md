Novel research that will disrupt the industry
================
Mr scientist
11 April, 2020

  - [Load data](#load-data)
  - [Don’t be afraid to add headers along the
    report](#dont-be-afraid-to-add-headers-along-the-report)
      - [They’ll all show up in the table of
        contents\!](#theyll-all-show-up-in-the-table-of-contents)
  - [There’s also plots and tables all
    around](#theres-also-plots-and-tables-all-around)
      - [gt tables in github\_document](#gt-tables-in-github_document)

<br>

# Load data

``` r
source("../passwords.R") # never post your passwords to Github again!
```

# Don’t be afraid to add headers along the report

<br>

## They’ll all show up in the table of contents\!

<br>

# There’s also plots and tables all around

``` r
plot(mtcars$mpg, mtcars$cyl)
```

![](README_files/figure-gfm/show%20a%20plot-1.png)<!-- -->

``` r
pandoc.table(head(mtcars[, 1:4]))
```

|                       | mpg  | cyl | disp | hp  |
| :-------------------: | :--: | :-: | :--: | :-: |
|     **Mazda RX4**     |  21  |  6  | 160  | 110 |
|   **Mazda RX4 Wag**   |  21  |  6  | 160  | 110 |
|    **Datsun 710**     | 22.8 |  4  | 108  | 93  |
|  **Hornet 4 Drive**   | 21.4 |  6  | 258  | 110 |
| **Hornet Sportabout** | 18.7 |  8  | 360  | 175 |
|      **Valiant**      | 18.1 |  6  | 225  | 105 |

<br>

## gt tables in github\_document

I’ve also found a nice workaround to incorporate tables from the **gt**
package.

You can create the table object:

``` r
# Define the start and end dates for the data range
start_date <- "2010-06-07"
end_date <- "2010-06-14"

# Create a gt table based on preprocessed
# `sp500` table data

a = sp500 %>%
  dplyr::filter(date >= start_date & date <= end_date) %>%
  dplyr::select(-adj_close) %>%
  gt() %>%
  tab_header(
    title = "S&P 500",
    subtitle = glue::glue("{start_date} to {end_date}")
  ) %>%
  fmt_date(
    columns = vars(date),
    date_style = 3
  ) %>%
  fmt_currency(
    columns = vars(open, high, low, close),
    currency = "USD"
  ) %>%
  fmt_number(
    columns = vars(volume),
    suffixing = TRUE
  ) 
```

And then at some point you can also view it using the `gt::gtsave`
function:

``` r
gtsave(a, "try.png")
```

![](README_files/figure-gfm/show%20gt%20table-1.png)<!-- -->

We next remove the resulting pic:

``` r
invisible(file.remove("try.png"))
```

It’s a little shorter and easier to implement then inserting the
resulting pic using standard markdown.
