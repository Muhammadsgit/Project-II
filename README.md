## Executive Summary:

This project focuses on building a regression model to predict house prices using the Ames Housing Dataset. The primary metric for model evaluation is the Root Mean Squared Error (RMSE). Linear regression serves as the main modeling approach, but other regression techniques like Lasso is also explored. Additionally, we will also experiment with Polynomial Features and Scaling. We will document the performance of each model with it's RMSE and R2 scores. In the end we will examine the forward selection and backward selection algorithms for determining optimal features for our regression model. We will conclude our exploration with the stepwise algorithm for feature selection and document our findings.

## Problem Statement:
The primary objective of this project is to determine the best regression model for predicting house prices based on the features in the Ames Housing Dataset. The success of the model will be evaluated using RMSE.


## File Directory/table of contents

    
![image](https://media.git.generalassemb.ly/user/50604/files/0c978e64-6410-41b9-bd8f-c9a076a60353)




## Data and Data Dictionary:

The primary dataset used in this project is the Ames Housing Dataset, which provides detailed information about various houses and their features. Below is a brief data dictionary for some of the primary features:

| Feature             | Type     | Description |
|---------------------|----------|-------------|
| SalePrice           | Integer  | Sale price of the house |
| Overall Qual        | Integer  | Overall material and finish of the house |
| Gr Liv Area         | Integer  | Above grade (ground) living area square feet |
| Garage Cars         | Integer  | Size of the garage in car capacity |
| Total Bsmt SF       | Integer  | Total square feet of the basement area |
| ...                 | ...      | ... |

Note: The above is a partial data dictionary. For a complete list of features and their descriptions, please refer to following  link: [Link text](https://jse.amstat.org/v19n3/decock/DataDocumentation.txt)


## Conclusions and Recommendations:

Based on the regression analysis of the Ames Housing Dataset:

- The simple linear regression model with the stepwise algorithm provided the best results in terms of $RMSE$ and $R^2$ score.
- Spending adequate time on feature engineering enhances the model's performance and guarentees improvements over baseline models.
- Given this model's predictive accuracy, real estate agencies and potential home buyers can use this as a tool for price estimation in the Ames area.

### Summary of all models

| Model Description                                               | RMSE                     | R2                        | Initial # Features | Final # Features (if applicable) |
|-----------------------------------------------------------------|--------------------------|---------------------------|--------------------|------------------|
| Model of highest correlated features                            | 40412.86100369427        | 0.7626541968542401        | 10                 | -                |
| Model of highest correlated features with Cross validation      | mean rmse = 36949.87866445592 | mean r2 = 0.779848655366105 | 10             | -                |
| Model of highest correlated features with Lasso                 | 44359.00408473574        | 0.7140395731173013        | 10                 | -                |
| Model of all numeric features                                   | 38337.59165478559        | 0.7864045402331978        | 37                 | -                |
| Model of all numeric features with Cross Validation             | mean rmse = 35642.85184537606 | mean r2 = 0.791738446278189 | 37            | -                |
| Model of all numeric features with Lasso                        | 37934.24414094182        | 0.7908753474821981        | 37                 | -                |
| Model of all features with dummied preprocessing                | 34243.128952623614       | 0.8295922881232749        | 209                | -                |
| Model of all features with dummied preprocessing and CV         | mean rmse = 34290.61380036194 | mean r2 = 0.8002326002217905 | 209          | -                |
| Model of all features with dummied preprocessing and Lasso     | 37934.24414094182        | 0.7908753474821981        | 209                | -                |
| Forward selection algorithm with numeric features only         | 37753.02406324579        | 0.7928686421507606        | 37                 | 33               |
| Forward selection algorithm with numeric and dummied features  | 33840.37573779651        | 0.8335772418404599        | 209                | 120              |
| Backward selection algorithm with numeric features only        | 41751.280747375204       | 0.7466727159535904        | 209                | 36               |
| Backward selection algorithm with numeric and dummied features | 35439.69000658719        | 0.8174750696856952        | 209                | 208                |

<br></br>
| Model Description (features converted to polynomial of degree 2)                                           | RMSE                   | R2                        | Initial # Features |
|-------------------------------------------------------------|------------------------|---------------------------|--------------------|
| Model with all numeric features and grid searching for best alpha | 38505.77372194258      | 0.7845263982307846        | 37                 |
| Model with LassoCV with numeric features only               | 38421.485445693455     | 0.7854686995389903        | 37                 |
| Model with LassoCV with numeric and dummied                 | 36777.60317703496     | 0.803433634559926        | 209                 |
| Model with all numeric features and *NaN filled with mean of data distribution*    | 23139.72146085574      | 0.9104218737234883        | 39                 |
 
<br></br>
| **Best performing and Final Model**                                               | RMSE                     | R2                        | Initial # Features | Final # Features (if applicable) |
|-----------------------------------------------------------------|--------------------------|---------------------------|--------------------|------------------|
| Model with all features trained using stepwise selection algorithm with simple linear regression    | 19455.7677        | 0.938694        | 221                 | 94                |

## Areas for Further Research/Study:

- Exploring more advanced regression techniques, such as ensemble methods and neural networks, to improve the prediction accuracy.
- Incorporating external data, such as economic indicators and housing market trends, to provide more context to the predictions.
- Conducting a deeper feature engineering and selection process to identify potentially overlooked features that could improve the model's performance even more!

## Sources:

- Ames Housing Dataset: [Link to dataset](https://www.kaggle.com/datasets/shashanknecrothapa/ames-housing-dataset)
- Practical Statistics for Data Scientists by Peter Bruce, Andrew Bruce, and Peter Gedeck

## Authors
- [Muhammad Affan Hassan](hassan.affan@gmail.com)
