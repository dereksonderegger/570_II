# Resampling Linear Models



```r
library(dplyr)
library(ggplot2)
library(ggfortify)
library(car)       # for the Boot function
library(boot)      # for the boot function
```

The last several chapters have introduced a number of parametric models where we assume that the error terms are normally distributed.
$$\begin{aligned}
  \textrm{One-sample t-test:}	& \;\;\; Y_{i}=\mu+\epsilon_{i}                      & \textrm{where} & \;\;\;\epsilon_{i}\stackrel{iid}{\sim}N\left(0,\sigma\right) \\
  \textrm{Two-sample t-test:}	&	\;\;\;Y_{ij}=\mu_{i}+\epsilon_{ij}                & \textrm{where} & \;\;\;\epsilon_{ij}\stackrel{iid}{\sim}N\left(0,\sigma\right)\;\;\;i\in\left\{ 1,2\right\} \\
  \textrm{ANOVA:}		          & \;\;\;Y_{ij}=\mu_{i}+\epsilon_{ij}                & \textrm{where} & \;\;\;\epsilon_{ij}\stackrel{iid}{\sim}N\left(0,\sigma\right)\;\;\;i\in\left\{ 1,2,\dots,k\right\} \\
  \textrm{Regression:}		    & \;\;\;Y_{i}=\beta_{0}+\beta_{1}x_{i}+\epsilon_{i} & \textrm{where} & \;\;\;\epsilon_{i}\stackrel{iid}{\sim}N\left(0,\sigma\right)
  \end{aligned}$$

We developed hypothesis tests and confidence intervals for the model parameters assuming that the error terms were normally distributed and, in the event that they are normally distributed, those tests and confidence intervals are the best we can do. However, if the errors are not normally distributed, what should we do?

Previously we used bootstrapping to estimate the sampling distribution of the sampling statistic when we didn't know the distribution. We will use the same bootstrapping method, but we'll simplify all of the above cases to the the same simple linear model 
$$Y_{i}=E\left(Y_{i}\right)+\epsilon_{i}\;\;\;\textrm{where}\;\;\epsilon_{i}\stackrel{iid}{\sim}N\left(0,\sigma\right)$$ 
and $E\left(Y_{i}\right)$ takes on some form of the parameters depending on the model specified. It turns out that R can do all of these analyses using the same `lm()` function we used in for regression.

**I will not be covering this Chapter.  If you would like more information please talk with me.  I have omitted the rest of the chapter to help be clear what I feel is important for the final exam.**
