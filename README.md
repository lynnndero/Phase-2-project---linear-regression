# Final Project Submission

Student name: LYNN WANJIKU NDERO

Student pace: full time

Scheduled project review date/time: 1 WEEK

Instructor name: ANTONNY MUIKO

[Presentation link](https://docs.google.com/presentation/d/1ZlQAi1Z28xvuozPVPxn7UfFtK87RZQouCMTwPfaP0o0/edit?usp=sharing)



 # PROJECT TITLE: HOME RENOVATIONS AND THEIR BENEFICIAL EFFECT ON HOME     ESTIMATED  VALUE

## OVERVIEW
This project is focused on home renovations and how it increases the estimated value of the homes. 

The first step getting the business understanding, data understanding and the objective of the project.

We begin by importing the data from the provided databases(csv file and .md file), opening and reading data.

We then prepare the data by cleaning it. This is by identifying any missing value, dropping the missing values and then checking for duplicates. Moreover, we formulate the hypothesis, null and alternative hypothesis

We first create dummy variables then build models, get the results from the models, represent them using different visualizations such as scatterplots with fitted regression lines. 

Finally, we deduced conclusions from the model findings.


## 1.BUSINESS UNDERSTANDING

Many homeowners face obstacles when it comes to home renovations resulting in outcomes such as delays, cost overrun among others.
They may need a slight push for them to believe that home renovations can help them get the maximum estimated value of their homes.
This is where real estate agency that help homeowners sell or/and buy houses comes in. The agency provides guidance on how renovating their homes can help them reach their objective of optimum home estimated value.

## DATA UNDERSTANDING

We need to explore how increasing measures/sizes of various house features such as floors will increase the overall price of the house/s.
This is by analysing the dataset provided by formulating the hypothesis of the project and building various regression models to aid in analysing the relationship between the dependable variable and independent variables.

## MAIN OBJECTIVE

The main objective of the project is to determine how renovations od various features such as square footing of living area leads to an increase in home estimated values.

## 2. LOADING DATA
Importing the relevant libraries

Opening the provided files using 'pd.read_csv' for the csv files and 'os' for the .md file

## 3. DATA PREPARATION
Using .info() formula to determine the number of entries in each column, their datatypes and if there are any missing values.

Using .shape function to know the total number of rows and columns.

Determining the number of houses renovated by looking at the 'yr_renovated' column in the dataset

Using .dropna() to drop all missing values

Checking for duplicates using .duplicated().sum()

Formulated null hpothesis that home renovations does not increase the estimated value of houses and alternative hypotheis that home renovations does increase the estimated value of houses.

## 4. MODELING
Created dummy variables from the data needed dataframe

Started with a baseline modeling with target variable, Price, and feature variable, Sqft_livings, that had the highest correlation.Together with visualizations. The summary of the results from the fitted model showed that an increase in sqft_living results to an increase in price. The model also showed a 50% variance in price.

Second modeling with target variable, Price, and one more feature, Sqft_above, that had the second highest correlation. Together with visualizatons. The results showed a similar variance as the baseline model of 50% but the price increased with an increase in sqft_living when considered while a small decrease in price when sqft_lot is considered.

Third modeling with target variable, Price and all the feature variables with numeric datatype. This resulted to a small increase in the variance to 52.3% and an increase in price when some features are considered.

Overall, not only was variance and coefficient observed but also the pvalues of both F-statistic and t-statistic shown in the summaries of the models.


## 5. REGRESSION RESULTS

After analysing using both the coefficients and graphs of the models, the more befitting results were from the coefficients due to better understanding and easier interpretation. The following are the resuls:

From baseline model:
1. The model explains about 50% variance in price.
2. The model is statistically significant overall with an F-statistic p-value below 0.05
2. The model's coefficients(const and sqft_living) are both statistically significant with a t-statictic p-values below 0.05
3. For an increase in sqft_living there is an associate increase in price by 286.15.
4. If sqft_living = 0, the price would be expected to be -55,160.00

From second model:
1. The model is statistically significant overall, with an F-statistic p-value well below 0.05
1. The model explains about 50% variance in price.
2. The model coefficients(const, sqft_living and sqt_above) are statistically significant with a t-statictic p-values below   0.05
3. For an increase in sqft_living there is an associate increase in price by 296.44.\
   We see that there is an increase from the previous model therefore showing that sqft_above has a meaningful confounding in the relationship between both sqft_living and price.
4. For an increase of 1 sqft_above, there is an associate decrease in price by -13.02.

From third model:
1. The model is statistically significant with a F-statistic p-value below 0.05
2. The model explains a 52.3% variance in price
   The R-squared increased by 2.3%
3. Most of the model coefficients are statistically significant:
   const, bedrooms, sqft_living, sqft_lot, yr_renovated and sqft_above have p-values below 0.05.
   bathrooms and floors have a coefficient greater than 0.05 meaning they have no effect on price thus statistically insignificant.
4. For an increase in sqft_living there is an associate increase in price by 335.\
   We see that there is an increase from the previous model therefore showing that other features have a meaningful confounding in the relationship between both sqft_living,sqft_above and price.

## 6. CONCLUSION

From assessing the three models using their coefficients rather than the graphs, there is an increase in the variation(R-Squared) from 50% to 52.3%.\
Though it is a small difference we can see that features such as bathrooms and floors, though with higher p-value than 0.05 have contributed to the increase in variance in price.\
We can conclude that upgrade of the features, such as , increasing bedrooms, sqft_lot, sqft_living and bathrooms increases the predicted target of price resulting in enhancment of livability, convience and becomes more appealing to buyers.\
Therefore, we reject our null hypothesis and accept the alternative.


