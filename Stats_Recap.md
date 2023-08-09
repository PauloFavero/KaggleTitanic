# Statistical Analysis Recap

## Variance

Variance is the spread of values in a dataset around its mean value. It tells you how
far each number in the dataset is from its mean. The formula for variance $s^2"$ is defined below:

$$s^2 = \frac{\sum[(x_i - x_{\mu})^2]}{n-1}$$

A large variance indicates that the numbers in the dataset are far from the mean and far
from each other. A small variance, on the other hand, indicates that the numbers are close
to the mean and to each other. A variance of 0 indicates that all the numbers in the
dataset are the identical. Finally, the valid value of variance is always a positive number
(0 or more).

## Standard Deviation

$$\sigma = \sqrt{s^2}$$

## Covariance 

In statistics, covariance is the measure of the directional relationship between two
random variables. A positive covariance indicates that both random variables tend to move upward or downward at the same
time. A negative covariance indicates that both variables tend to move away from each other — when one moves
upward the other moves downward, and vice versa. When two random variables are independent, the covariance will be zero.
However, the reverse is not necessarily true — a covariance of zero does not mean that 2 random variables are
independent (a non-linear relationship can still exist between 2 random variables that
has zero covariance).

The covariance between two random variables X and Y is calculated using the following formula:

$$
cov_{x,y} = \frac{\sum[(x_i - x_{\mu})(y_i - y_{\mu})]}{n-1}
$$

where:
- $\text{cov}(X, Y)$ is the covariance between X and Y.
- $\mu_X$ is the mean of the random variable X.
- $\mu_Y$ is the mean of the random variable Y.


## Correlation

The correlation between two random variables measures both the strength
and direction of a linear relationship that exists between them. There are two ways
to measure correlation:

- *Pearson Correlation Coefficient* — captures the strength and direction of the
linear association between two continuous variables

- *Spearman’s Rank Correlation Coefficient* — determines the strength and
direction of the monotonic relationship which exists between two ordinal
(categorical) or continuous variables.


### Pearson Correlation Coefficient

The formula for the Pearson Correlation Coefficient is:


$$ r= \frac{\text{cov}(x, y) }{\sigma_{x}\sigma_{y}}$$

Like covariance, the sign of the pearson correlation coefficient indicates the
direction of the relationship. However, the values of the Pearson correlation
coefficient is contrained to be between -1 and 1. Based on the value, you can deduce
the following degrees of correlation:

- Perfect — values near to ±1
- High degree — values between ±0.5 and ±1
- Moderate degree — values between ±0.3 and ±0.49
- Low degree — values below ±0.29
- No correlation — values below ±0.29


### Spearman’s Rank Correlation Coefficient

If your data is not linearly distributed, you should use Spearman’s Rank Correlation
Coefficient instead of the Pearson Correlation Coefficient. The Spearman’s Rank
Correlation Coefficient is designed for distributions that are monotonic.

$$\rho = 1 - \frac{6 \sum d_i^2}{n(n^2 - 1)}$$

Where d is the difference in rank between the 2 random variables.

*Note:* Apply both the methods and check which is performing well. For
instance if results show spearman rank correlation coefficient is greater than
Pearson coefficient, it means your data has monotonic relationships and not
linear (just like the above example).

## Collinearity and Multicollinearity

*Collinearity* is when two features are linearly
associated (high correlation), and they are used as predictors for the target.

*Multicollinearity* is a special case of collinearity where a feature exhibits a linear
relationship with two or more features.

To reduce multicollinearity we are going to use the *VIF* method which stands for *Variance Inflation Factor*

VIF allows you to determine the strength of the correlation between the various
independent variables. It is calculated by taking a variable and regressing it against
every other variables.
VIF calculates how much the variance of a coefficient is inflated because of its linear
dependencies with other predictors.

VIF formula: 


$$ VIF = \frac{1}{1-R^2}$$

A large VIF indicates that this feature exhibits multicollinearity with the other
features. A small VIF indicates that this feature exhibits low multicollinearity
with the other features.

*Note:* While correlation matrix and scatter plots can be used to find multicollinearity, they only
show the bivariate relationship between the independent variables. VIF ,on the other
hand, shows the correlation of a variable with a group of other variables.


## References

- [Understaing Variance, Covariance and Correlation](https://towardsdatascience.com/statistics-in-python-understanding-variance-covariance-and-correlation-4729b528db01)
- [Understanding Colinearity and MultiColinearity](https://towardsdatascience.com/statistics-in-python-collinearity-and-multicollinearity-4cc4dcd82b3f)
