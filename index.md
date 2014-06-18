---
title       : Fuel Consumption Prediction based on 'Motor Trend Car Road Tests'
subtitle    : Course Project for Develop Data Products
author      : Wargamer1988
job         : Student
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
---

## Purpose of Web App

1. Predict the fuel consumption based on the entered values of automobile attributes.
2. The forecasting model is estimated from the dataset: Motor Trend Car Road Tests.
3. The data was extracted from the 1974 Motor Trend US magazine, and comprises fuel consumption and 10 aspects of automobile design and performance for 32 automobiles.



```r
head(mtcars, n=5)
```

```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
```

-----------------------------------

## How to Use

#### To check the records in dataset: Motor Trend Car Road Tests

1. Click the column header to sort a column
2. Change the number of records in display

#### To use the calculator the user must enter the following information

1. Weight (lb/1000, Min:3 Max:6)
2. 1/4 mile time (sec, Min:15 Max:20)
3. Transmission (0 = automatic, 1 = manual)

#### The calculator will then take the input information and output the predicted fuel consumption

-----------------------------------

## Model Explanation

#### The model estimation


```
##             Estimate Std. Error t value  Pr(>|t|)
## (Intercept)    9.618     6.9596   1.382 1.779e-01
## wt            -3.917     0.7112  -5.507 6.953e-06
## qsec           1.226     0.2887   4.247 2.162e-04
## am             2.936     1.4109   2.081 4.672e-02
```
With the backward-elmination strategy, the above model could be obtained.

#### The calculator works as follows:

* Calculates the fuel consumption as

_Fuel Consumption = -3.9165 * Weight + 1.2259 * 1/4 mile time + 2.9358 * Transmission_

-----------------------------------

## Example

1. If a user inputs a car:
 + weight = 3000 lb
 + 1/4 mile time = 17 sec
 + Transmission = Manual 
2. Then the calculator will output the fuel consumption:


```
## [1] 21.94
```

