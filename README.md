# StepReg
:exclamation: This is a read-only mirror of the CRAN R package repository.  StepReg — Stepwise Regression Analysis  
1. Introduction

What is stepwise regression?

Stepwise regression is a method of fitting regression models in which the choice of predictive variables is carried out by an automatic procedure.

What is the main features in SteReg?

In this package, multiple dependent variables stepwise regression and continous effect nesting within class effect are considered. It computes power for three test statistics: Wilks’ lambda, Pillai-Bartlett trace, and Hotelling Lawley trace in multivariate stepwise regression analysis.

2. Statistical and coding details in this package

The main approaches:

 Forward selection, which involves starting with no variables in the model, testing the addition of each variable using a chosen model fit criterion, adding the variable (if any) whose inclusion gives the most statistically significant improvement of the fit, and repeating this process until none improves the model to a statistically significant extent.
	
Backward elimination, which involves starting with all candidate variables, testing the deletion of each variable using a chosen model fit criterion, deleting the variable (if any) whose loss gives the most statistically insignificant deterioration of the model fit, and repeating this process until no further variables can be deleted without a statistically significant loss of fit.
	
Hybrid Approaches, a combination of the above, testing at each step for variables to be included or excluded.
	
Selection Criterion:

AIC/AICc/BIC/HQ/HQc/SBC/Pvalue based on F test and Approximate F test (Wilks’ lambda, Pillai-Bartlett trace, and Hotelling Lawley trace).
	
Multicollinearity:

Multicollinearity is a state of very high intercorrelations or inter-associations among the independent variables. The statistical inferences made about the data may not be reliable due to multicollinearity. In this package, multicollinearity is detected with tolerance and its reciprocal, called variance inflation factor (VIF).
	
Coding:

The core part of the program is coded with R and Cpp.

3. Usage and Examples

	#install.package("StepReg")
	library(StepReg)
	stepwise(data, y, notX, include, Class, selection, select, sle, sls, tolerance,Trace, Choose)
	Examples are listed with help of function stepwise()
	
We welcome commits from researchers who wish to improve our software, good luck to you.
