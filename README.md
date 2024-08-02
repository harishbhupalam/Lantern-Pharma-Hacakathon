# Lantern-Pharma-Hackathon
 
Organised by Lantern Pharma Inc. (Nasdaq: LTRN), the problem was to develop Machine Learning (ML) Prediction Models for Responses from four drugs and two combinations on Cancerous Tissues. The challenge was in the shape of the data. Contrary to traditional datasets with few features and numerous instances/observations, this data was wide with a whopping 16,000 features and just about 50 observations to train the models.

Approach and Methodology:

Given the small number of observations, the approach was to over-sample the training data to give the models a good chance to learn enough about the data. A small partition of training data was used for validation (oversampling was done after splitting to ensure validation was accurate).  The approach differed from oversampling only positive classes to random sampling both classes, based on the distribution of target variables of different drugs and combinations.
The most important step was to reduce the dimensionality through methods like PCA and Lasso and then check for the initial accuracy using various models. We observed that PCA and lasso were giving similar results in terms of accuracy. Since Logistic Regression (with L1 regularization) is more interpretable, we used that model.

Difference between single and combination drugs:

For all the single drugs, lasso with a default penalty of 1 gave the best results. For the combination of Mitomycin and Fulvestrant drugs, a higher penalty of 200 gave us the best results. The approach for Rapamycin-Gefitinib combination was to use a Meta-Logistic-Regression Classifier based on the individual drug responses. We used the predictions of the Rapamycin and Gefitinib as the independent variables for a logistic Regression. This method proved to be very effective and also impressed the judges
