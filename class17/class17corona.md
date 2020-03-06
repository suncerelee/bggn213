Untitled
================

Coronavirus
-----------

Here we analyze infection data for the 2019 novel Coronavirus COVID-19 (2019-nCoV) epidemic. The raw data is pulled from the Johns Hopkins University Center for Systems Science and Engineering (JHU CCSE) Coronavirus repository.

``` r
url <- "https://tinyurl.com/COVID-2019"
virus <- read.csv(url)

tail(virus)
```

    ##      Province.State Country.Region      Lat     Long       date cases      type
    ## 2881         Shanxi Mainland China  37.5777 112.2922 2020-03-05     2 recovered
    ## 2882        Sichuan Mainland China  30.6171 102.7103 2020-03-05    19 recovered
    ## 2883        Tianjin Mainland China  39.3054 117.3230 2020-03-05     4 recovered
    ## 2884       Victoria      Australia -37.8136 144.9631 2020-03-05     3 recovered
    ## 2885       Xinjiang Mainland China  41.1129  85.2401 2020-03-05     1 recovered
    ## 2886       Zhejiang Mainland China  29.1832 120.0934 2020-03-05    10 recovered

> Q1. How many total infected cases are there around the world?

``` r
total_cases <- sum(virus$cases)
total_cases
```

    ## [1] 155031

Lets have a look at the *$type* column

``` r
table(virus$type)
```

    ## 
    ## confirmed     death recovered 
    ##      1593       212      1081

> Q2. How many deaths linked to infected cases have there been?

``` r
inds <- virus$type == "death"
death_cases <- sum(virus[inds,"cases"])
death_cases
```

    ## [1] 3348

> Q3. What is the overall death rate?

``` r
round(death_cases/total_cases * 100, 2)
```

    ## [1] 2.16

> Q4. What is the death rate in "Mainland China"?

``` r
library(tidyverse)
```

    ## ── Attaching packages ──────────────────────────────────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.2.1     ✓ purrr   0.3.3
    ## ✓ tibble  2.1.3     ✓ dplyr   0.8.4
    ## ✓ tidyr   1.0.2     ✓ stringr 1.4.0
    ## ✓ readr   1.3.1     ✓ forcats 0.4.0

    ## ── Conflicts ─────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
mainland_china <- virus%>%
  filter(Country.Region == "Mainland China")

death_rate_mc <- mainland_china%>%
  group_by(type)%>%
  summarize_if(is.numeric, sum)%>%
  ungroup()%>%
  mutate(rate = cases/sum(cases)*100)

death_rate_mc%>%
  filter(type == "death")%>%
  select(rate)
```

    ## # A tibble: 1 x 1
    ##    rate
    ##   <dbl>
    ## 1  2.22

> Q5. What is the death rate in Italy, Iran and the US?

``` r
library(DescTools)
death_rate_all <- virus%>%
  group_by(type, Country.Region)%>%
  summarize_if(is.numeric, sum)%>%
  ungroup()%>%
  group_by(Country.Region)%>%
  mutate(rate = cases/sum(cases)*100)

death_rate_all%>%
  filter(Country.Region %like any% c("Italy", "Iran", "US"),
         type == "death")%>%
  select(Country.Region, rate)
```

    ## # A tibble: 3 x 2
    ## # Groups:   Country.Region [3]
    ##   Country.Region  rate
    ##   <fct>          <dbl>
    ## 1 Iran            2.45
    ## 2 Italy           3.35
    ## 3 US              4.98
