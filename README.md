# KaggleTitanic
Repository to solve the Kaggle Titatanic competition (https://www.kaggle.com/competitions/titanic/overview)


## Variable Notes

*pclass*: A proxy for socio-economic status (SES)
1st = Upper
2nd = Middle
3rd = Lower

*age*: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

*sibsp:* The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

*parch:* The dataset defines family relations in this way...
Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children travelled only with a nanny, therefore parch=0 for them.


## Next Steps:

- Improve data exploration with better graphics
- Handle missing values with a KNN Inputer
- Do some feature engineering
- Prepare data for training 
- Train the Classifiers

## References

- [Feature Engineering](https://triangleinequality.wordpress.com/2013/09/08/basic-feature-engineering-with-the-titanic-data/)
- [Normalization vs Standarization](https://towardsdatascience.com/normalization-vs-standardization-explained-209e84d0f81e)
- [Colinearity](https://towardsdatascience.com/statistics-in-python-collinearity-and-multicollinearity-4cc4dcd82b3f)