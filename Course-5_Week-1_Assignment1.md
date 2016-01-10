# Course 5: Reproducible Research: Week-1 Assessment-1


```r
library(dplyr)
```

## Loading and preprocessing the data

```r
actMon <- read.csv("activity.csv")
actMon_by_Days <- group_by(actMon, date) %>% summarize(Total.Steps = sum(steps, na.rm = TRUE))
```

## What is mean total number of steps taken per day?

```r
hist(actMon_by_Days$Total.Steps,
     breaks = 25,
     col = "light blue",
     xlab = "Steps",
     freq = TRUE,
     main = "Total Number of Steps taken per day")
```

![](Course-5_Week-1_Assignment1_files/figure-html/unnamed-chunk-3-1.png)\

```r
summary(actMon_by_Days)
```

```
##          date     Total.Steps   
##  2012-10-01: 1   Min.   :    0  
##  2012-10-02: 1   1st Qu.: 6778  
##  2012-10-03: 1   Median :10395  
##  2012-10-04: 1   Mean   : 9354  
##  2012-10-05: 1   3rd Qu.:12811  
##  2012-10-06: 1   Max.   :21194  
##  (Other)   :55
```



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?

