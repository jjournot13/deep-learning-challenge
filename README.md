# deep-learning-challenge

## Overview
The purpose of this project was to develop a tool that the nonprofit foundation, Alphabet Soup, could use to select applicants for funding that have the best chance of success in their ventures. Implementing what we've learned about machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

The dataset contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within the dataset are a number of columns that capture metadata about each organization, including:

- EIN and NAME — Identification columns
- APPLICATION_TYPE — Alphabet Soup application type
- AFFILIATION — Affiliated sector of industry
- CLASSIFICATION — Government organization classification
- USE_CASE — Use case for funding
- ORGANIZATION — Organization type
- STATUS — Active status
- INCOME_AMT — Income classification
- SPECIAL_CONSIDERATIONS — Special considerations for application
- ASK_AMT — Funding amount requested
- IS_SUCCESSFUL — Was the money used effectively


## Results

Data Preprocessing
- IS_SUCCESSFUL was used as the target for the model.
- EIN and NAME were removed from the data.
- All remaining factors were used as features.

Compiling, Training, and Evaluating the Model
The initial model included two hidden relu layers and the sigmoid output layer and returned an accuracy of 0.7259474992752075.

To optimize the model to reach at least 75% accuracy, I adjusted the model several ways:

1. I created bins for the 'ASK_AMT' moving everything greater than 5000 into a single bin.


2. Next, I kept the 'ASK_AMT' bins and increased the ephochs from 100 to 150.


3. Finally, I added a third hidden relu layer.


## Summary

Overall, each iteration of the model produced consistent accuracy scores between 72% and 74%. While I was able to get close to the target of 75% with my second optimization attempt, I would be interested to see if a residual network model would work better for this dataset.