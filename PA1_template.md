---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---


## Loading and preprocessing the data

data <- read.csv("activity.csv")

head(data)


## What is mean total number of steps taken per day?

# Calculate the total number of steps taken per day


total_Steps_per_day <- aggregate(steps ~ date , data, FUN = sum)

total_Steps_per_day


#  histogram of the total number of steps taken each day

hist(total_Steps_per_day$steps) 



## What is the average daily activity pattern?
total_Steps_per_day <- sum(data$steps, na.rm = T)
total_Steps_per_day



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
