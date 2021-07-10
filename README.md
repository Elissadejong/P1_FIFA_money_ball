# P1_FIFA_money_ball

## Project objective
In this research, we attempt to realize when the market value of a footballer is optimal for transfer in FIFA21. As well, 3 musings that arose from the dataset were answered using both SQL and Python.  

## Data download and description
The data was downloaded using pandas. The data contains detailed information about the footballers of FIFA21. After viewing the data, a general cleaning was performed. This included standardizing the headers of the columns, setting the index to the variable 'ID', removing symbols from values, converting values to appropriate values (e.g. K to value multiplied by 1000) and changing the datatypes of certain values.

## Questions
1. How do the top 10 ranked club squads in FIFA21 differ in their footballers' mentalities?
Different aspects of footballer's mentalities were taken from the explanation of the variables on sofifa.com. To answer this question, SQL was used. From interpreting the results we can, for example, see that Juventus ranks very high in all aspects of footballers' mentalities except for 'positioning', 'vision' and 'composure'. On the grounds of these results, coaches of opponent teams could adjust their tactics.   
2. Does the time since a footballer joined the team influence their overall rating with respect to their potential?
To obtain an answer to this question, pandas groupby function was used and it yielded a nice result. The longer the duration footballers are in a team, the lesser their overall rating differs from their potential rating (strongly correlated, -0.89). Possible future analysis could check if this correlation is also significant.  
3. Do footballers with a left foot preference have a better wrong foot rating than their right footed colleagues?
Fewer footballers have a left foot preference, which is why it was hypothesized that these footballers may hold an advantage on their wrong foot rating, as opposed to footballers with a right foot preference. However, the results showed an opposite result, except for the category of the 2* wrong-foot rating. 

## Data cleaning and selection
After cleaning the data in two parts (general cleaning and targeted cleaning), the variables were selected for the data model. Unfortunately I was a "tad" limited by the time left before the deadline, so I choose the variables mainly on my own thoughts of which variables would determine market value. Null values were checked and dealt with, BoxCox was done, the categorical variables were converted into dummies, and outliers were taken care of. Looking back, I think maybe my model would've been better if I had normalized/ standardized the data.    

## Visualization 

## Results
I ran into quite some problems when concating the two dataframes, getting a bunch of NaN-values in the model dataframe. In "the final hour" I finally managed to locate the problem (the indices of the two dataframes were not aligned) and was able to fit and train a model with a R2 of 0.633. However, in real life, I would keep working on the linear regression model to obtain a better R2 score. As for now, there are a few significant variables in the model that determine a footballer's market value, with 'age' yielding the biggest correlation.    

## List of libraries
 https://www.kaggle.com/ekrembayar/fifa-21-complete-player-dataset
 
 Thank you for taking the time to look at my very first Data Analytics project! :))