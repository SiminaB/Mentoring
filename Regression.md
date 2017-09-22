# Everything in statistical modeling can be seen as a regression

This is of course a bit of an exaggeration! It also depends on the way things are emphasized in, for example, statistical
graduate programs. I know that my own training program was highly focused on seeing much of statistics as either a
special case or a generalization of some kind of linear regressio model. I kind of love this view and try to emphasize it whenever I can
to collaborators, although I do admit that sometimes you have to start from special cases in order to build up the whole.

## Regression concepts connected to loss functions and conditional means and medians

Regression basically refers to modelling the average effect of a variable (called the outcome or the dependent variable, and
often denoted by Y) given some other variables (called the explanatory or independent variables, and often denoted by 
X<sub>1</sub>, X<sub>2</sub>
etc). In more statistical terms this can be defined as the
["conditional expectation of the dependent variable given the independent variables,"](https://en.wikipedia.org/wiki/Regression_analysis)
although, as I will explain later, one can see "average" as a more general measure of the "center" of the distribution,
which is not necessarily the "expected value."

The simplest case of regression is that of linear regression with a single explanatory variable. In other words, trying to
draw a "best fit line" through a scatterplot. There are many ways to define the "best fit" and the one that is usually
considered is based on the [quadratic loss function](https://en.wikipedia.org/wiki/Loss_function#Quadratic_loss_function) 
(also known as squared error loss or L<sub>2<\sub> loss.)
Basically, if one seeks to *minimize the sum of the squares of the differences* between the true outcome Y and the fitted values on the
line hat{Y}, the solution is the "usual" [ordinary least squares (OLS)](https://en.wikipedia.org/wiki/Ordinary_least_squares).
If there is no explanatory variable, the fitted line is flat and represents the average (mean) value of the explanatory
values.
In general, the OLS has some nice properties, for example if the error terms - defined as \epsilon = Y - \beta<sub>0<\sub> - 
\beta<sub>1<\sub> X<sub>1<\sub>, where 
\beta<sub>0<\sub> and \beta<sub>1<\sub> are the true intercept and slope of the line - are independent and identically distributed with finite
variance, the OLS fit is an unbiased estimator of the conditional mean E(Y|X) (i.e. its mean is equal to the conditional
mean) and is in fact the [minimum-variance unbiased estimator](https://en.wikipedia.org/wiki/Minimum-variance_unbiased_estimator).
Note that so far I haven't discussed the distribution of Y or even whether Y is continuous. However, in the case where the errors
(and therefore Y conditional on X) are normally distributed, the OLS is also the maximum likelihood estimator (MLE) of the conditional mean
E(Y|X). 

One reason why the quadratic loss function is considered very often is because the mathematics works out very nicely (can solve for the maximum using the usual calculus-based second
derivative test). This also generalizes nicely if there are more explanatory variables - we can just include them all in a matrix
X and essentially proceed in the same way with the help of some multivariate calculus. 
There are however many other ways of defining the "best fit."
However, perhaps one is interested in
estimating an aspect of the distribution of Y|X other than its mean, such as its median.
The median is naturally connected to the [absolute loss](https://en.wikipedia.org/wiki/Loss_function)
(also known as as the L<sub>1<\sub> loss) in the same way that the mean is connected to the 
quadratic error loss. In this case, the criterion is to *minimize the sum of the absolute values of the differences*
between the true outcome and the fitted values, also called the 
[least absolute deviations or least absolute residuals](https://en.wikipedia.org/wiki/Least_absolute_deviations).
In the absence of an explanatory variable, the flat fitted line represents the median of the explanatory values.
If we look more generally for a function f where the values f(X) are most similar to Y, with the similarity being 
defined using the quadratic loss, then the "best fit" (which minimizes
[the expected prediction error (EPE - see _Elements of statistical learning_, section 2.4)](https://web.stanford.edu/~hastie/Papers/ESLII.pdf) is the function
f(x) = E(Y|X=x) (conditional mean); by contrast, if it is defined using the absolute loss, it is
f(x) = median(Y|X=x) (conditional median). In general, medians are more robust than means, given their lack of dependence
on outliers, but the math gets harder much faster due to discontinuous derivatives which complicate optimization procedures.
Similarly, if a [step function (0-1) loss](https://en.wikipedia.org/wiki/Loss_function#0-1_loss_function) is used instead,
the result is f(x) = mode(Y|X=x) (conditional mode). *Add Manski paper here!!* Note that the mean, median, and mode
are the most common ways of describing the "center" of a continuous distribution.
 
It may also be of interest to consider another quantile besides the median, which is sometimes the case
when considering a variable with an asymmetric distribution, such as income distributions. 
[Quantile regression](https://en.wikipedia.org/wiki/Quantile_regression) considers different loss functions 
for this purpose. If the errors have an asymmetric Laplace distribution, the estimator obtained here for a specific quantile is 
its [MLE](http://www.american.edu/cas/economics/info-metrics/pdf/upload/working-paper-bera.pdf).

## From weighted regression to general linear models

## T-tests, ANOVA, and all the rest: Hypothesis testing in linear models

## Smoothing and regression

## Regression and machine learning
