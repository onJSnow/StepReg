# StepReg
:exclamation: This is a read-only mirror of the CRAN R package repository.  StepReg — Stepwise Regression Analysis  
## 1. Introduction

* What is the stepwise regression?

Stepwise regression is a method of fitting regression models in which the choice of predictive variables is carried out by an automatic procedure.

* What is the main features in SteReg?

In this package, multiple dependent variables stepwise regression, continous effect nested within class effect and forced first n effects are considered. It computes power for three test statistics in multivariate stepwise regression analysis: Wilks’ lambda, Pillai-Bartlett trace, and Hotelling Lawley trace.

## 2. Statistical and coding details in this package

* The main approaches:
* * Forward selection, which involves starting with no variables in the model, testing the addition of each variable using a chosen model fit criterion, adding the variable (if any) whose inclusion gives the most statistically significant improvement of the fit, and repeating this process until none improves the model to a statistically significant extent.
	
* * Backward elimination, which involves starting with all candidate variables, testing the deletion of each variable using a chosen model fit criterion, deleting the variable (if any) whose loss gives the most statistically insignificant deterioration of the model fit, and repeating this process until no further variables can be deleted without a statistically significant loss of fit.
	
* * Hybrid Approaches, a combination of the above, testing at each step for variables to be included or excluded.
	
* Selection or Choose Criterion:

AIC/AICc/BIC/HQ/HQc/SBC/Pvalue based on F test and Approximate F test (Wilks’ lambda, Pillai-Bartlett trace, and Hotelling Lawley trace).
	
* Multicollinearity:

Multicollinearity is a state of very high intercorrelations or inter-associations among the independent variables. The statistical inferences made about the data may not be reliable due to multicollinearity. In this package, multicollinearity is detected with tolerance and its reciprocal, called variance inflation factor (VIF).
	
* Coding:

The core part of the program is coded with R and Cpp.

## 3. Usage and Examples
	#install.package("StepReg")
	
	library(StepReg)
	
	stepwise(data, y, notX, include, Class, weights, selection, select, sle, sls, tolerance,Trace, Choose)
	
	Examples are listed with help of function stepwise()
	
## 4.Validation
* Reference

Result of multivariate stepwise regression are consistent with the reference
* SAS software validation

The final results from this package are validated with SAS software,

data set1 without class effect: 13 dependent variable, 129 independent variable and 216 samples.

data set2 with 4 class effect: 12 dependent variable, 1270 independent variable and 647 samples.

data set3 with 6 class effect: 5 dependent variable, 2068 independent variable and 412 samples.

We welcome commits from researchers who wish to improve our software, and good luck to you.
