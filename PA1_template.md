---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---

## Load some libraries

```r
library(dplyr)
##library(tidyr)
##library(ggplot2)
```

## Loading and preprocessing the data
Load the data file

```r
df <- read.csv("activity.csv")
```

Convert the date column to the date class

```r
df$date <- as.Date(df$date)
```

## What is mean total number of steps taken per day?

Group the data by date and apply the dplyr summarize function to
calculate the total number of steps taken per day

```r
groups <- group_by(df,date)
summarise(groups,sum(steps))
```

```
## Source: local data frame [61 x 2]
## 
##          date sum(steps)
##        (date)      (int)
## 1  2012-10-01         NA
## 2  2012-10-02        126
## 3  2012-10-03      11352
## 4  2012-10-04      12116
## 5  2012-10-05      13294
## 6  2012-10-06      15420
## 7  2012-10-07      11015
## 8  2012-10-08         NA
## 9  2012-10-09      12811
## 10 2012-10-10       9900
## ..        ...        ...
```

Make a histogram of the total number of steps taken each day


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
