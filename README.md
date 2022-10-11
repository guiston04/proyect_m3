# Diamonds and ML

# Problem description

    The objective of this project is to predict the price of a diamond knowing a list of characteristic that define it. 
    In order to predict the right price with minimum error, we need first to identify which of the provided 
    characteristics drive the price up or down and then what model is better suited to make the prediction.

# Analysis

    The analysis has been divided in two. One analysis had the objective to understand the dataset and what 
    conclusions about the price we could get (EDA) and the second analysis focused on getting more knowledge about the 
    fundamentals of the diamonds business.

    The EDA analysis gave us some clues about what are the main drivers of the price of a diamond. This analysis pointed 
    to carat, color, clarity, dimensions and cut as the characteristics that have the most impact on the diamond final 
    price.

    The fundamentals analysis confirmed what we saw in the EDA. Diamonds prices are defined by what the industry call 
    the 4 Cs, which are carat, cut, clarity and color. This analysis also gave us new important insights about what 
    defined the price of a diamond and these are that the dimensions should be proportionate and that the diamond 
    should be colored or uncolored but not in the middle.

    We can conclude then that we will center our focus on the 4Cs to develop our machine learning problem.

# Features

    The features we chose to predict the price of the diamonds are cut, carat, clarity and color. We have completed 
    those with two calculated features: good_color (which indicates groups of colors that affect prices) and the depth 
    of the diamond (z/y).

# Models

    We have created two ensemble models which are the results of the average prediction of 4 differente models. These 
    models are Random Forest, Neural Network, CatBoost model and XGBoost.

    The two models presented use a weighted average of the predictions in function of the RMSE. The most important 
    models are Neural Network and Catboost and the least are the Random Forest and Xgboost.

    The main difference between the two models is one of the feature: good_color. For one of the models, good colors 
    indicates that J is totally colored and D totally uncolored, which would affect the price if true. And the 
    other one, indicates two groups of diamonds with different coloration, uncolored (D,E,F) and slightly 
    colored (J, H, I, G) that would affect price in a different manner.

# Conclusions

    It is clear that the four Cs are greatly correlated with the price of the diamonds. The most complicated 
    part to predict the price is the weight that the models give to the feature in order to predict it. In order to 
    improve the different model, it is key to keep looking for new information about this industry. 
