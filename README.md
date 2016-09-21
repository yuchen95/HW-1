Homework 1
================

You are currently in the GitHub repository (repo) for `HW-1`. You must have completed all the steps in [Setting Up](https://rudeboybert.github.io/MATH216/jekyll/update/2016/09/12/getting-started.html).

Learning Goals
--------------

-   Using the `dplyr` and `ggplot2` packages, getting experience
    -   manipulating/cleaning/visualizing real, messy, and complex data
    -   performing extensive data cleaning exploratory data analysis (EDA)
-   Familiarizing yourself with R Markdown, a tool for reproducible research. If your `.Rmd` file won't knit, take a look at the [debugging sheet](https://docs.google.com/document/d/1P7IyZ4On9OlrCOhygFxjC7XhQqyw8OludwChz-uFd_o/edit).
-   Developing good programming practices. For example, Google has their own [R Style Guide](https://google.github.io/styleguide/Rguide.xml). Give it a look, but don't worry about getting it all right the first time, I'll be giving feedback as the semester progresses.
-   For those of you new to involved programming/coding, learning that [Google](https://xkcd.com/627/) is your best friend.

Homework
--------

1.  Follow the same workflow as in <a target="_blank" class="page-link"
    href="https://github.com/2016-09-Middlebury-Data-Science/HW-0#homework">HW-0</a> for HW-1.
2.  Do not submit a `HW-1.Rmd` file that does not knit.
3.  I anticipate you spending between 8-12 total (across all submissions) on this homework.

Data
----

All domestic flights leaving George Bush Intercontinental Airport (IAH) in Houston in 2011. There are 5 data sets to consider:

-   `flights` \[227,496 x 14\]: Flight data.
-   `weather` \[8,723 x 14\]: Hourly weather data.
-   `planes` \[2,853 x 9\]: Plane metadata.
-   `airports` \[3,376 x 7\]: Airport metadata.
-   `states` \[48 x 3\]: (Lower 48) state data.

Tips
----

1.  Keep different projects compartmentalized using RStudio Projects. You can quickly switch between them by clicking the RStudio logo in the top right of RStudio.
2.  Work in groups as per the ideas of collaborative learning. However, keep in mind the guidelines under Evaluation -&gt; Homework in the [syllabus](https://rudeboybert.github.io/MATH216/syllabus/).
3.  Do not spin your wheels for more than 20 minutes. This takes self-awareness and mindfulness. After 20 minutes of frustration, take a break and/or seek help.
4.  Take a look at the `knitr::kable()` function:

``` r
library(knitr)
library(dplyr)

# Take only first five rows:
output <- mtcars %>% 
  slice(1:5)

# Compare this output:
output
```

    ##    mpg cyl disp  hp drat    wt  qsec vs am gear carb
    ## 1 21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
    ## 2 21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
    ## 3 22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
    ## 4 21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
    ## 5 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2

``` r
# with this one:
output %>% kable()
```

|   mpg|  cyl|  disp|   hp|  drat|     wt|   qsec|   vs|   am|  gear|  carb|
|-----:|----:|-----:|----:|-----:|------:|------:|----:|----:|-----:|-----:|
|  21.0|    6|   160|  110|  3.90|  2.620|  16.46|    0|    1|     4|     4|
|  21.0|    6|   160|  110|  3.90|  2.875|  17.02|    0|    1|     4|     4|
|  22.8|    4|   108|   93|  3.85|  2.320|  18.61|    1|    1|     4|     1|
|  21.4|    6|   258|  110|  3.08|  3.215|  19.44|    1|    0|     3|     1|
|  18.7|    8|   360|  175|  3.15|  3.440|  17.02|    0|    0|     3|     2|
