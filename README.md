<!-- badges: start -->
[![R-CMD-check](https://github.com/Quanlin222/Four/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/Quanlin222/Four/actions/workflows/R-CMD-check.yaml)
<!-- badges: end -->

# Four package

In this package, we create a package to handle linear regression models. 
We use the QR decomposition to create the most basic functionality in the R package and implement the results as an S3 class.
We also implement an object oriented system to handle special functions such as print(), plot(), resid(), pred(), coef() and summary().


## 1.1 Install package

devtools::install_github("Quanlin222/Four")

## 1.2 Load package

library(Four)

## 1.3 Load data

data(iris)

lin_obj <- linreg(Petal.Length ~ Sepal.Width + Sepal.Length, data = iris)

## 1.4 Run the linreg() function

### 1.4.1 Print out the coefficients and coefficient names:

print(lin_obj)

### 1.4.2 Plot:

plot(lin_obj)

### 1.4.3 The vector of residuals e_hat:

resid(lin_obj)


### 1.4.4 The predicted values y_hat:

pred(lin_obj)


### 1.4.5 The coefficients as a named vector:

coef(lin_obj)

### 1.4.6 Present the coefficients with their standard error, t-value and p-value as well as the estimate of σ_hat and the degrees of freedom:

summary(lin_obj)
