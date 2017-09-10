# Everything in statistical modeling can be seen as a regression

This is of course a bit of an exaggeration. It also depends on the way things are emphasized in, for example, statistical
graduate programs. I know that my own training program was highly focused on seeing much of statistics as either a
special case or a generalization of some kind of linear model. I kind of love this view and try to emphasize it whenever I can
to collaborators, although I do admit that sometimes you have to start from special cases in order to build up the whole.

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
Basically, if one seeks to minimize the sum of squares of the differences between the true outcome Y and the fitted values on the
line hat{Y}, the solution is the "usual" [ordinary least squares (OLS)](https://en.wikipedia.org/wiki/Ordinary_least_squares).
This has some nice properties, for example if the error terms - defined as \epsilon = Y - \beta_0 - \beta_1 X_1, where 
\beta_0 and \beta_1 are the true intercept and slope of the line - are independent and identically distributed with finite
variance, the OLS fit is an unbiased estimator of the conditional mean E(Y|X) (i.e. its mean is equal to the conditional
mean) and is in fact the [minimum-variance unbiased estimator](https://en.wikipedia.org/wiki/Minimum-variance_unbiased_estimator).
Note that so far I haven't discussed the distribution of Y or even whether Y is continuous. However, in the case where Y
(and therefore the errors) are normally distributed, the OLS is also the maximum likelihood estimator of the conditional mean
E(Y|X).

There are many other ways of defining the "best fit" and in fact one of the reasons why the quadratic loss function is considered
most often is because the mathematics works out very nicely (can solve for the maximum using the usual calculus-based second
derivative test). This also generalizes nicely if there are more explanatory variables - we can just include them all in a matrix
X and essentially proceed in the same way with the help of some multivariate calculus. However, perhaps one is interested in
estimating an aspect of the distribution of Y|X other than its mean - perhaps its median or another quantile. This is often
of interest when considering a variable with an asymmetric distribution, such as income distributions. Thus, a 
different loss function may be used for this purpose, resulting in [quantile regression](https://en.wikipedia.org/wiki/Quantile_regression).



