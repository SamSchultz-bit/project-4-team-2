# Spam E-Mail Predictor
### Contributors
Angel Lee, Sam Schultz, Matthew Byron, Esther Baumgartner, Colin Vehmeier

## Overview
### Problem:
Do you ever find unnecesary spam emails in your primary inbox or worse have to go looking for a ham email in your spam/junk folders?

### Description:

The aim of this project is to create a classification model that can accurately sort whether an email is spam or ham. 
> Spam: unsolicited and unwanted junk email sent out in bulk to an indiscriminate

> Ham: non-spam email, “good/wanted” email

## Repository Structure:

In this repository, you will find the Google Slides presentation, the results folder, the resources folder, and the cleaning.ipynb file where we cleaned our data, ran our models, and made changes to optimize them. The results folder contains the classification reports for each model before and after optimization changes. The resources folder that contains the main_ham folder and the main_spam folder with the raw data (retrieved from Kaggle). 

TLDR:
- Main: Google Slides Presentatio, Results folder, Resource Folder, and Cleaning jupyter notebook.
  - Results folder: Classification reports
  - Resources folder: main_ham and main_spam folders

## Data Source and Explanation:

The dataset used was the "Email Spam Dataset (Extended) retrieved from Kaggle (cited below in resources). The original source is SpamAssasin's Old Public Corpus but was uploaded by a Kaggle user. The dataset has two zip folders. The main_ham folder contains 6,951 'ham' emails and the main_spam folder contains 2,398 'spam' raw email files. All of the data was collected from 2002-2005.

## Data Cleaning and Preprocessing:

We must give credit to the original contributer, the user Maharshipandya from Kaggle. They contributed the notebook "Email Spam Classification [98%]" (also linked below in resource). Their notebook helped us successfully load and parse the files. We also made tweaks for how we structured our project.

### Steps:
1. Load ham and spam emails
2. Parse email files
3. BeautifulSoup to convert Raw Email files to text
4. Count word frequencies
5. Convert the word counts of any email to a vector
6. Create pipeline
7. Prepare and train test sets
8. Run classification models
9. Make adjustments to optimize models and rerun

### Models Used:
Random Forest: "Ensemble of decision trees. Each tree is built with randomness to improve generalization and reduce overfitting. Used for both classification and regression."

Logistic Regression: "Linear model predicting probabilities for binary classification. Extends to multinomial logistic regression for multiple classes."

Decision Tree: "Tree-like model with nodes representing features and leaves representing outcomes. Used for both classification and regression."

## Results:

### Before:

### After:

## Resources

**Dataset:**

SpamAssasin's Old Public Corpus. (n.d.). Email Spam Dataset (Extended). Kaggle. Retrieved from: https://www.kaggle.com/datasets/maharshipandya/email-spam-dataset-extended

**Cleaning:**

Pandaya, M. (n.d.). Email Spam Classification [98%]. Kaggle. Retrieved from:https://www.kaggle.com/code/maharshipandya/email-spam-classification-98

**Defining Spam:**

Cisco. (n.d.). What Is Spam Email? Cisco. Retrieved from: https://www.cisco.com/c/en/us/products/security/email-security/what-is-spam.html

**Defining Ham:**

Cwiki. (2009, September 20th). Ham. CWiki. Retrieved from: https://cwiki.apache.org/confluence/display/spamassassin/Ham#:~:text=%22Ham%22%20is%20e%2Dmail,non%2Dspam%22%2C%20instead

**Optimizing Random Forest Model:**

Koehrsen, W. (2018, January 9th). Hyperparameter Tuning the Random Forest in Python. Retrieved from: https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74

**Optimizing Logistic Regression Model:**

StackOverflow. (2023, March 10th). How to increase the model accuracy of logistic regression in Scikit python? StackOverflow. Retrieved from: https://stackoverflow.com/questions/38077190/how-to-increase-the-model-accuracy-of-logistic-regression-in-scikit-python

**Optimizing Decision Tree Model:**

StackOverflow. (2020, June 5th). Improve precision of my predictive technique in Python. StackOverflow. Retrieved from: https://stackoverflow.com/questions/62224518/improve-precision-of-my-predictive-technique-in-python

**Understanding Confusion Matrix:**

Narkhede, S. (2018, May 9th). Understanding Confusion Matrix. Medium. Retrieved from: https://towardsdatascience.com/understanding-confusion-matrix-a9ad42dcfd62

**Markdown:**

Parr, K. (2022, August 22nd). Markdown Cheat Sheet- How to Write Articles in Markdown Language. FreeCodeCamp. Retrieved from: https://www.freecodecamp.org/news/markdown-cheatsheet/

**Defining Models:**
OpenAI. (n.d.) Can you explain to me what Random Forest, Logistic Regression, and Decision Tree models are? Retrieved on 2023, December 6th. Retrieved from: https://chat.openai.com/
