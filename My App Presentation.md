My App Presentation
========================================================
author: Santiago Puentes Navas
date: 12/03/2020
autosize: true

Lineal Regression of Sequence with Added Noise
========================================================

For this project, I have decided to create a useful app that showcases the effect of random noise added to a simple sequence (X axis).
This added noise gets displayed on the Y axis, while allowing the user to adjust three variables: The data size (number of points), the mean and the standard deviation of the random noise.

Rationale
========================================================

The purpose behind this project is to help people with a visual guide on how random noise might alter the results of an otherwise simple linear proportion (y equals to x). This project also shows how it can affect a linear regression and show the graphic results of trying to fit a linear model with different numbers of datapoints, and a heavier or lighter effect from the noise.
In the next slide I will showcase the basic code used to perform this project. The app URL is https://spuentes95.shinyapps.io/FinalProject/

Code example
========================================================

```r
#Using default numbers, in the app these variables can be changed by the user
number_of_datapoints <- 30
noise_mean <- 5
noise_sd <- 15
x <- 1:number_of_datapoints
noise_add <- rnorm(number_of_datapoints, mean = noise_mean, sd = noise_sd)
y <- x + noise_add
model_fit = lm(y ~ x)
```

Slide With Plot
========================================================

![plot of chunk unnamed-chunk-2](My App Presentation-figure/unnamed-chunk-2-1.png)
