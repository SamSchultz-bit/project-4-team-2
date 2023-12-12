# Spam E-Mail Predictor
### Contributors
Angel Lee, Sam Schultz, Matthew Byron, Esther Baumgartner, Colin Vehmeier

## Overview
### Problem:
- Receiving too many spam emails in your inbox
- Having to find a ham email in your spam/junk folders

### Description:

The aim of this project is to create a classification model that can accurately sort whether an email is spam or ham. 
> Spam: unsolicited and unwanted junk email sent out in bulk to an indiscriminate

> Ham: non-spam email, “good/wanted” email

## Repository Structure:

In this repository, you will find the Google Slides presentation, the results folder, the resources folder, and the cleaning.ipynb file where we cleaned our data, ran our models, and made changes to optimize them. The results folder contains the classification reports for each model before and after optimization changes. The resources folder that contains the main_ham folder and the main_spam folder with the raw data (retrieved from Kaggle). 

TLDR:
- Main: Google Slides Presentation (Project-4-Group-2: Ham vs Spam), Results folder, Resources Folder, and Cleaning jupyter notebook.
  - Results folder: Classification reports and visualizations
  - Resources folder: main_ham and main_spam folders

## Data Source and Explanation:

The dataset used was the "Email Spam Dataset (Extended) retrieved from Kaggle (cited below in resources). The original source is SpamAssasin's Old Public Corpus but was reuploaded and modified by the Kaggle user. The dataset has two zip folders for spam and ham emails. The main_ham folder contains 6,951 'ham' emails and the main_spam folder contains 2,398 'spam' raw email files. All of the data was collected from 2002-2005.

## Data Cleaning and Preprocessing:

We must give credit to the original contributer, Kaggle user Maharshipandya. Along with reuploading the dataset with extendsions, they also contributed the notebook "Email Spam Classification [98%]" (also linked below in resource). Their notebook helped us successfully load, parse, and clean the raw data. We also made adjustments to their original code for how we structured our project.

### Steps:
1. Load ham and spam emails
2. Parse email files
3. BeautifulSoup to convert Raw Email files to text
4. Count word frequencies
5. Convert the word counts of any email to a vector
6. Create pipeline
7. Prepare and train test sets
8. Run classification models
9. Make optimizations to best model and rerun

### Models Tested:
Random Forest: "Ensemble of decision trees. Each tree is built with randomness to improve generalization and reduce overfitting. Used for both classification and regression."

Logistic Regression: "Linear model predicting probabilities for binary classification. Extends to multinomial logistic regression for multiple classes."

Decision Tree: "Tree-like model with nodes representing features and leaves representing outcomes. Used for both classification and regression."

## Results:
##### Note about Confusion Matrix

[[True Negative (TN), False Positive (FP)][False Negative (FN), True positive (TP)]]

True Positives (TP): These are the emails that the model correctly identified as spam. This is good because it means the spam filter is doing its job correctly.

True Negatives (TN): These are the emails that the model correctly identified as ham (non-spam). This is also good as it indicates that non-spam emails are being correctly identified.

False Positives (FP): These are the emails that are actually ham, but the model incorrectly classified them as spam. False positives can be annoying because they may lead to important emails being flagged as spam.

False Negatives (FN): These are the emails that are actually spam, but the model incorrectly classified them as ham. False negatives are a more serious issue because they allow spam to reach the inbox, defeating the purpose of the spam filter.

1. Random Forest: 99% Accuracy, TP- 465, TN- 1378, FP- 8, FN- 19.

2. Logistic Regression: 98% Accuracy, TP- 465, TN- 1369, FP- 17, FN- 19.

3. Decision Tree: 97% Accuracy, TP- 449, TN- 1360, FP- 26, FN- 35.

**The Random Forest Model performed the best and is the model we are choosing to optimize.**

### After Optimizing the Random Forest Model:

## Resources (In Usage Order):

**Dataset:**

Maharshipandya. (n.d.). Email Spam Dataset (Extended). Kaggle. Retrieved from: https://www.kaggle.com/datasets/maharshipandya/email-spam-dataset-extended

Spam Assassin’s Old Public Corpus. (n.d.). Index of/old/publiccorpus. Apache Software Foundation. Retrieved from: https://spamassassin.apache.org/old/publiccorpus/ 

**Cleaning:**

Pandaya, M. (n.d.). Email Spam Classification [98%]. Kaggle. Retrieved from:https://www.kaggle.com/code/maharshipandya/email-spam-classification-98

**Defining Spam:**

Cisco. (n.d.). What Is Spam Email? Cisco. Retrieved from: https://www.cisco.com/c/en/us/products/security/email-security/what-is-spam.html

**Defining Ham:**

Cwiki. (2009, September 20th). Ham. CWiki. Retrieved from: https://cwiki.apache.org/confluence/display/spamassassin/Ham#:~:text=%22Ham%22%20is%20e%2Dmail,non%2Dspam%22%2C%20instead

**Understanding Confusion Matrix:**

Narkhede, S. (2018, May 9th). Understanding Confusion Matrix. Medium. Retrieved from: https://towardsdatascience.com/understanding-confusion-matrix-a9ad42dcfd62

**Markdown:**

Parr, K. (2022, August 22nd). Markdown Cheat Sheet- How to Write Articles in Markdown Language. FreeCodeCamp. Retrieved from: https://www.freecodecamp.org/news/markdown-cheatsheet/

**Defining Models:**
OpenAI. (n.d.) Can you explain to me what Random Forest, Logistic Regression, and Decision Tree models are? Retrieved on 2023, December 6th. Retrieved from: https://chat.openai.com/

**Optimizing Model(s):**

Koehrsen, W. (2018, January 9th). Hyperparameter Tuning the Random Forest in Python. Retrieved from: https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74

StackOverflow. (2023, March 10th). How to increase the model accuracy of logistic regression in Scikit python? StackOverflow. Retrieved from: https://stackoverflow.com/questions/38077190/how-to-increase-the-model-accuracy-of-logistic-regression-in-scikit-python

StackOverflow. (2020, June 5th). Improve precision of my predictive technique in Python. StackOverflow. Retrieved from: https://stackoverflow.com/questions/62224518/improve-precision-of-my-predictive-technique-in-python

SciKit Learn. (n.d.). Sklean.model_selection.RandomizedSearchCV. Scikit Learn Documentation. Retrieved from: https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html 

StackOverflow. (n.d.). Proper use of “class_weight” parameter in Random Forest classifier. StackOverflow. Retrieved from: https://stackoverflow.com/questions/58275113/proper-use-of-class-weight-parameter-in-random-forest-classifier

StackOverflow. (n.d.). How to penalize False Negatives more than False positives. StackOverflow. Retrieved from: https://stackoverflow.com/questions/49151325/how-to-penalize-false-negatives-more-than-false-positives

Scikit Learn. (n.d.). Sklearn.ensemble.RandomForestClassifier. SciKit Learn Documentation. Retrieved from: https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html

Brownlee, J. (2021, January 5th). Random Oversampling and Undersampling for Imbalanced Classification. Machine Learning Mastery. Retrieved from: https://machinelearningmastery.com/random-oversampling-and-undersampling-for-imbalanced-classification/

