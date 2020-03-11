Untitled
================

Read sample genotypes data from ENSEMBLE
----------------------------------------

We downloaded genotype data from ENSEMBLE on the MXL Mexican Ancestry in Los Angeles, California dataset

What proportion of this data are G/G etc?

``` r
mxl <- read.csv("373531-SampleGenotypes-Homo_sapiens_Variation_Sample_rs8067378.csv")

mxl
```

    ##    Sample..Male.Female.Unknown. Genotype..forward.strand. Population.s. Father
    ## 1                   NA19648 (F)                       A|A ALL, AMR, MXL      -
    ## 2                   NA19649 (M)                       G|G ALL, AMR, MXL      -
    ## 3                   NA19651 (F)                       A|A ALL, AMR, MXL      -
    ## 4                   NA19652 (M)                       G|G ALL, AMR, MXL      -
    ## 5                   NA19654 (F)                       G|G ALL, AMR, MXL      -
    ## 6                   NA19655 (M)                       A|G ALL, AMR, MXL      -
    ## 7                   NA19657 (F)                       A|G ALL, AMR, MXL      -
    ## 8                   NA19658 (M)                       A|A ALL, AMR, MXL      -
    ## 9                   NA19661 (M)                       A|G ALL, AMR, MXL      -
    ## 10                  NA19663 (F)                       A|A ALL, AMR, MXL      -
    ## 11                  NA19664 (M)                       G|A ALL, AMR, MXL      -
    ## 12                  NA19669 (F)                       A|A ALL, AMR, MXL      -
    ## 13                  NA19670 (M)                       A|A ALL, AMR, MXL      -
    ## 14                  NA19676 (M)                       G|G ALL, AMR, MXL      -
    ## 15                  NA19678 (F)                       A|A ALL, AMR, MXL      -
    ## 16                  NA19679 (M)                       A|G ALL, AMR, MXL      -
    ## 17                  NA19681 (F)                       A|G ALL, AMR, MXL      -
    ## 18                  NA19682 (M)                       A|G ALL, AMR, MXL      -
    ## 19                  NA19684 (F)                       A|G ALL, AMR, MXL      -
    ## 20                  NA19716 (F)                       G|A ALL, AMR, MXL      -
    ## 21                  NA19717 (M)                       A|G ALL, AMR, MXL      -
    ## 22                  NA19719 (F)                       G|G ALL, AMR, MXL      -
    ## 23                  NA19720 (M)                       G|G ALL, AMR, MXL      -
    ## 24                  NA19722 (F)                       G|A ALL, AMR, MXL      -
    ## 25                  NA19723 (M)                       G|G ALL, AMR, MXL      -
    ## 26                  NA19725 (F)                       A|G ALL, AMR, MXL      -
    ## 27                  NA19726 (M)                       A|A ALL, AMR, MXL      -
    ## 28                  NA19728 (F)                       A|A ALL, AMR, MXL      -
    ## 29                  NA19729 (M)                       A|G ALL, AMR, MXL      -
    ## 30                  NA19731 (F)                       A|A ALL, AMR, MXL      -
    ## 31                  NA19732 (M)                       A|G ALL, AMR, MXL      -
    ## 32                  NA19734 (F)                       G|A ALL, AMR, MXL      -
    ## 33                  NA19735 (M)                       G|G ALL, AMR, MXL      -
    ## 34                  NA19740 (F)                       A|A ALL, AMR, MXL      -
    ## 35                  NA19741 (M)                       A|A ALL, AMR, MXL      -
    ## 36                  NA19746 (F)                       A|A ALL, AMR, MXL      -
    ## 37                  NA19747 (M)                       G|A ALL, AMR, MXL      -
    ## 38                  NA19749 (F)                       A|G ALL, AMR, MXL      -
    ## 39                  NA19750 (M)                       A|G ALL, AMR, MXL      -
    ## 40                  NA19752 (F)                       A|G ALL, AMR, MXL      -
    ## 41                  NA19755 (F)                       A|A ALL, AMR, MXL      -
    ## 42                  NA19756 (M)                       G|A ALL, AMR, MXL      -
    ## 43                  NA19758 (F)                       A|G ALL, AMR, MXL      -
    ## 44                  NA19759 (M)                       G|A ALL, AMR, MXL      -
    ## 45                  NA19761 (F)                       G|A ALL, AMR, MXL      -
    ## 46                  NA19762 (M)                       A|A ALL, AMR, MXL      -
    ## 47                  NA19764 (F)                       A|A ALL, AMR, MXL      -
    ## 48                  NA19770 (F)                       A|G ALL, AMR, MXL      -
    ## 49                  NA19771 (M)                       A|A ALL, AMR, MXL      -
    ## 50                  NA19773 (F)                       A|A ALL, AMR, MXL      -
    ## 51                  NA19774 (M)                       A|G ALL, AMR, MXL      -
    ## 52                  NA19776 (F)                       A|G ALL, AMR, MXL      -
    ## 53                  NA19777 (M)                       A|A ALL, AMR, MXL      -
    ## 54                  NA19779 (F)                       G|A ALL, AMR, MXL      -
    ## 55                  NA19780 (M)                       A|A ALL, AMR, MXL      -
    ## 56                  NA19782 (F)                       G|A ALL, AMR, MXL      -
    ## 57                  NA19783 (M)                       A|G ALL, AMR, MXL      -
    ## 58                  NA19785 (F)                       A|A ALL, AMR, MXL      -
    ## 59                  NA19786 (M)                       G|A ALL, AMR, MXL      -
    ## 60                  NA19788 (F)                       A|G ALL, AMR, MXL      -
    ## 61                  NA19789 (M)                       G|G ALL, AMR, MXL      -
    ## 62                  NA19792 (M)                       A|A ALL, AMR, MXL      -
    ## 63                  NA19794 (F)                       G|A ALL, AMR, MXL      -
    ## 64                  NA19795 (M)                       A|G ALL, AMR, MXL      -
    ##    Mother
    ## 1       -
    ## 2       -
    ## 3       -
    ## 4       -
    ## 5       -
    ## 6       -
    ## 7       -
    ## 8       -
    ## 9       -
    ## 10      -
    ## 11      -
    ## 12      -
    ## 13      -
    ## 14      -
    ## 15      -
    ## 16      -
    ## 17      -
    ## 18      -
    ## 19      -
    ## 20      -
    ## 21      -
    ## 22      -
    ## 23      -
    ## 24      -
    ## 25      -
    ## 26      -
    ## 27      -
    ## 28      -
    ## 29      -
    ## 30      -
    ## 31      -
    ## 32      -
    ## 33      -
    ## 34      -
    ## 35      -
    ## 36      -
    ## 37      -
    ## 38      -
    ## 39      -
    ## 40      -
    ## 41      -
    ## 42      -
    ## 43      -
    ## 44      -
    ## 45      -
    ## 46      -
    ## 47      -
    ## 48      -
    ## 49      -
    ## 50      -
    ## 51      -
    ## 52      -
    ## 53      -
    ## 54      -
    ## 55      -
    ## 56      -
    ## 57      -
    ## 58      -
    ## 59      -
    ## 60      -
    ## 61      -
    ## 62      -
    ## 63      -
    ## 64      -

We want to look at the second column that contains the genotype information

``` r
table(mxl$Genotype..forward.strand.)
```

    ## 
    ## A|A A|G G|A G|G 
    ##  22  21  12   9

RNA-Seq result analysis for different genotypes of this SNP
-----------------------------------------------------------

``` r
expr <- read.table("rs8067378_ENSG00000172057.6.txt")
head(expr)
```

    ##    sample geno      exp
    ## 1 HG00367  A/G 28.96038
    ## 2 NA20768  A/G 20.24449
    ## 3 HG00361  A/A 31.32628
    ## 4 HG00135  A/A 34.11169
    ## 5 NA18870  G/G 18.25141
    ## 6 NA11993  A/A 32.89721

``` r
plot(expr$geno, col="pink")
```

![](class15_files/figure-markdown_github/unnamed-chunk-4-1.png)

``` r
summary(expr[ expr$geno == "G/G",]$exp)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   6.675  16.903  20.074  20.594  24.457  33.956

``` r
hist(expr[expr$geno == "G/G",]$exp, breaks=20)
```

![](class15_files/figure-markdown_github/unnamed-chunk-6-1.png)

``` r
summary(expr[ expr$geno == "A/G",]$exp)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   7.075  20.626  25.065  25.397  30.552  48.034

``` r
hist(expr[expr$geno == "A/G",]$exp, breaks=20)
```

![](class15_files/figure-markdown_github/unnamed-chunk-8-1.png)

``` r
summary(expr[ expr$geno == "A/A",]$exp)
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   11.40   27.02   31.25   31.82   35.92   51.52

``` r
hist(expr[expr$geno == "A/A",]$exp, breaks=20)
```

![](class15_files/figure-markdown_github/unnamed-chunk-10-1.png)

Try a boxplot
-------------

We will use the `boxplot()` function and the input data will be **expr**. How do we draw a useful plot?

``` r
boxplot(exp ~ geno, data=expr, notch=T)
```

![](class15_files/figure-markdown_github/unnamed-chunk-11-1.png)

How many samples are we looking at here?

``` r
nrow(expr)
```

    ## [1] 462
