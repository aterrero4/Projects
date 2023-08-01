# Introduction
## Background
### Ames Iowa and the Housing Dataset
Ames, Iowa is a city located in the central part of the U.S. state of Iowa, in Story County, and it is part of the Ames, Iowa Metropolitan Statistical Area, which is a part of the larger Ames-Boone, Iowa Combined Statistical Area. As of the 2020 census, the city population was around 66,500. Ames is the home of Iowa State University (ISU), a public research university with leading Agriculture, Design, Engineering, and Veterinary Medicine colleges.

The Ames housing market is somewhat competitive. In 2021, homes in Ames received 3 offers on average and sold in around 19 days. The average sale price of a home in Ames was approximately $215K in 2021, with a trend of price increase over the years. However, please note that these statistics may change based on the current year and market dynamics. More about the city can be found [Here](https://www.cityofames.org/about-ames/about-ames#:~:text=Based%20on%20the%202020%20census,the%20school%20year%20or%20longer.&text=The%20City%20Manager%20is%20the%20City's%20chief%20administrator.)

The Ames, Iowa housing dataset, which is often used in machine learning, was compiled by Dean De Cock, a professor of statistics at Truman State University. It was intended to be a modernized and expanded alternative to the well-known Boston Housing dataset. It includes 79 explanatory variables describing nearly every aspect of residential homes in Ames, making it an excellent dataset for data exploration and predictive modeling.

In the dataset, each row represents a unique property sale, and the variables capture many aspects of what a typical home buyer would want to know about a property. This includes straightforward attributes like the number of bedrooms and bathrooms, the size of the living room, and the number of garage spaces, to more detailed variables like the type of roofing material, the condition of the garage, and the number of fireplaces.

### Problem Statement

Garages, as part of a property's attributes, can contribute significantly to the property's overall value. Garages provide additional utility and storage, and in some areas, are considered a necessity. This can be particularly true in places that experience severe weather, where a garage can provide protection for vehicles and other belongings. In addition, having a garage can enhance a property's appeal to prospective buyers, leading to a higher sale price.

For Ames, Iowa, a city with a population of over 60,000 people and home to Iowa State University, it would be reasonable to hypothesize that properties with garages might command higher prices. This could be due to a number of factors, including the convenience of having secure, on-site parking and additional storage, and the fact that a garage can be a desirable feature for families and individuals living in this city.

The analysis of the Ames Housing dataset can help determine whether the presence, size, and condition of garages have a significant impact on housing prices. By utilizing statistical techniques, such as correlation analysis and regression models, you can quantify the relationship between these variables.

## Data Sources
*(http://www.cityofames.org/assessor/)
## Data Documentation
*(https://jse.amstat.org/v19n3/decock/DataDocumentation.txt)

# Data Analysis
Our analysis started with examining the relationship between garage characteristics and the sale price of houses. We focused on various garage features such as the type of garage, its finishing quality, the condition, and the number of cars it can contain. The data revealed insights about the potential role of a garage in determining the sale price of a house in Ames, Iowa.

We then created a linear regression model to establish a quantitative relationship between the garage features and the house prices. This model achieved an R-squared score of approximately 0.59, indicating a moderate level of explanation of the variance in the house prices by the garage features.

To improve our model, we applied a Lasso regression, a method that performs both variable selection and regularization to enhance the prediction accuracy and interpretability. The initial Lasso model, without tuning the hyperparameters, scored 0.6045 on the training data and 0.6005 on the validation data. These scores are slightly higher than those of the linear model, which suggests a minor improvement in the prediction accuracy.

In a bid to extract the maximum predictive power of our Lasso model, we used a grid search strategy to find the best hyperparameters. This technique uses cross-validation to evaluate the model performance for each combination of the provided hyperparameters, selecting the combination that gives the highest score. We varied the alpha parameter, which controls the amount of shrinkage: the larger the value of alpha, the greater the amount of shrinkage and thus the coefficients become more robust to collinearity. We also tested different values for max_iter which is the maximum number of iterations for the model to run.

The grid search revealed that the Lasso model achieved the best performance with an alpha of approximately 78.48 and max_iter of 1000. This optimized Lasso model scored 0.5849, slightly lower than the initial Lasso model but still higher than the linear model.

# Conclusions
In conclusion, our analysis suggests that garage features do play a significant role in determining house prices in Ames, Iowa. The optimized Lasso model, with its built-in feature selection capability, provides an effective tool for predicting house prices based on garage features. However, as the scores indicate, there are other factors not captured by garage features that also affect the sale price, necessitating a more comprehensive model for more accurate predictions.