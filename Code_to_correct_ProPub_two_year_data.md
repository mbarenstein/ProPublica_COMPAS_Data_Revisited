Code to Correct ProPublica Two-Year Dataset
================
Matias Barenstein

This file contains the **R code** one can use to **implement** the
simple **April 1, 2014, COMPAS screening date cutoff** rule I use in my
paper to correct ProPublica’s **two-year general recidivism** dataset.
(This code also appears in my *Rmarkdown* program in this repository,
titled *ProPub\_COMPAS\_Revisited\_analysis.Rmd*, which generates all
the Figures and Tables in my paper)

``` r
# Reading in ProPublica's two-year general recidivism dataset
df_propub_2_yr_csv <- read.csv(
  'https://raw.githubusercontent.com/propublica/compas-analysis/master/compas-scores-two-years.csv', 
  as.is = TRUE)

df_propub_2_yr_csv$compas_date_numeric <- as.numeric(as.Date(df_propub_2_yr_csv$compas_screening_date))

nrow(df_propub_2_yr_csv)
```

    ## [1] 7214

``` r
# # April 1, 2014
# as.Date(16161, origin="1970-01-01")
# [1970-01-01 is R's internal date origin]

df_propub_2_yr_csv$post_april_2014 <- ifelse(df_propub_2_yr_csv$compas_date_numeric > 16161, 1, 0)

#############################

# Corrected two-year general recidivism dataset - 6216 total

# 7214 goes down by 998 people (all recidivists) to 6216
# This is the reduction in sample size when I implement 4/1/2014 cutoff
corrected_compas_two_year <- df_propub_2_yr_csv[which(df_propub_2_yr_csv$post_april_2014==0),]

nrow(corrected_compas_two_year)
```

    ## [1] 6216

``` r
# # Could write permanent corrected two-year general recidivism file
# write.csv(corrected_compas_two_year, file = "CORRECTED_compas_two_year.csv")

#############################
```

As shown in my research paper, this drops **998** ***recidivists*** who
ProPublica incorrectly kept in the two-year (general recidivism)
dataset. I drop them because they have COMPAS screen dates post-April 1,
2014.
