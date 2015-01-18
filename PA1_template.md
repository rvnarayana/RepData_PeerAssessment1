---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---

Question1

## Loading and preprocessing the data


```r
measures <- read.csv("activity.csv", stringsAsFactors=FALSE)
head(measures)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```

## What is mean total number of steps taken per day?


```r
q1 <- aggregate(measures$steps, by=list(measures$date), FUN=sum, na.rm=TRUE)
colnames(q1) <- c("ActivityDate", "TotalSteps")
hist(q1$TotalSteps, xlab = "Total Steps", col="red")
```

![plot of chunk unnamed-chunk-2](figure/unnamed-chunk-2.png) 

```r
print(paste("Mean value of Total Number of Steps Daily = ", mean(q1$TotalSteps)))
```

```
## [1] "Mean value of Total Number of Steps Daily =  9354.22950819672"
```

```r
print(paste("Median value of Total Number of Steps Daily = ", median(q1$TotalSteps)))
```

```
## [1] "Median value of Total Number of Steps Daily =  10395"
```
## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
