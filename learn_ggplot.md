---
title: "R for Data Science"
output: 
  html_document:
    keep_md: true
---

This is a [R Markdown](http://rmarkdown.rstudio.com) Notebook.  Pressing *Ctrl+Shift+Enter* runs the chunk. 


```r
library(gapminder)
```

```
## Warning: package 'gapminder' was built under R version 3.4.3
```

```r
library(dplyr)
```

```
## Warning: package 'dplyr' was built under R version 3.4.3
```

```
## 
## Attaching package: 'dplyr'
```

```
## The following objects are masked from 'package:stats':
## 
##     filter, lag
```

```
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
```

```r
library(ggplot2)
```

```
## Warning: package 'ggplot2' was built under R version 3.4.3
```

*Insert Chunk* on the toolbar or by pressing *Ctrl+Alt+I*.

When you save the notebook, an HTML file containing the code and output will be saved alongside it (click the *Preview* button or press *Ctrl+Shift+K* to preview the HTML file). The keep_md; true flag makes sure we also keep an intermediate markdown file with output which can be displayed on github.

Unlike *Knit*, *Preview* does not run any R code chunks, what was last run in the editor is displayed.


```r
gapminder_1952 = gapminder %>% filter(year==1952)
```

```
## Warning: package 'bindrcpp' was built under R version 3.4.4
```

```r
ggplot(gapminder_1952, aes(x=gdpPercap, y = lifeExp, size= pop)) +
   geom_point() + scale_x_log10() + scale_y_log10() + facet_wrap(~ continent)
```

![](learn_ggplot_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

