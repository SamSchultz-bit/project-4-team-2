# Spam E-Mail Predictor
### Contributors
Angel Lee, Sam Schultz,  Colin Vehmeier, Matthew Byron, Esther Baumgartner,

## Overview
### Problem:
- Receiving too many spam emails in your inbox
- Having to find a ham email in your spam/junk folders

### Description:

The aim of this project is to create a classification model that can accurately sort whether an email is spam or ham. 
> Spam: unsolicited and unwanted junk email sent out in bulk to an indiscriminate

> Ham: non-spam email, “good/wanted” email

## Repository Structure:

In this repository, you will find the "Project-4-Group-2_Ham vs Spam" Google Slides presentation, the "Results" folder, the "Resources" folder, and the "model_optimized" jupyter notebook where we cleaned our data, ran our models, made optimizations, and visualizations. The "Results" folder contains the confusion matrix heatmaps for each model and precision-recall scatter plots. The "Resources" folder contains the main_ham folder and the main_spam folder with the raw data (retrieved from Kaggle). 

TLDR:
- Main: "Project-4-Group-2_Ham vs Spam" Google Slides Presentation, "Results" folder, "Resources Folder", and "model_optimized" jupyter notebook.
  - Results folder: Confusion Matrix Heatmaps and Precision-Recall Scatter Plots
  - Resources folder: "main_ham" and "main_spam" folders

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
##### Confusion Matrix Explanation:

True Positives (TP): These are the emails that the model correctly identified as spam. This is good because it means the spam filter is doing its job correctly.

True Negatives (TN): These are the emails that the model correctly identified as ham (non-spam). This is also good as it indicates that non-spam emails are being correctly identified.

False Positives (FP): These are the emails that are actually ham, but the model incorrectly classified them as spam. False positives can be annoying because they may lead to important emails being flagged as spam.

False Negatives (FN): These are the emails that are actually spam, but the model incorrectly classified them as ham. False negatives are a more serious issue because they allow spam to reach the inbox, defeating the purpose of the spam filter.

### Initial Run:
![cm-heat-decisiontree-1](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/baa36f4a-b8cf-444f-b128-10c5e294c91d)
![cm-heat-logisticreg-1](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/0b3de01c-f133-46db-86e3-1fa9a4270fa0)
![cm-heat-randomforest-1](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/b4a32c22-57f2-4333-a059-17e1b43d8b7e)
![precision-recall-scatter-1](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/3555f003-f2bf-4202-8285-0b763b925b88)

### Oversampled Run:
![cm-heat-decisiontree-2-oversam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/6ef04ea6-b6e9-4891-a4c1-feffcba3fc54)
![cm-heat-logisticreg-2-oversam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/6c5193f8-167c-47f1-a70c-b0efca072087)
![cm-heat-randomforest-2-oversam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/29255724-6afe-44bd-8c73-18aa1243a2db)
![precision-recall-scatter-2-oversam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/c1a3fed7-1350-42f1-a6df-3b5a9d9b86f7)

### Undersampled Run:
![cm-heat-decisiontree-3-undersam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/162b97b2-b97d-44ad-ba93-8830a946563a)
![cm-heat-logisticreg-3-undersam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/088ef99b-259a-495b-b947-0276ff09486f)
![cm-heat-randomforest-3-undersam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/3c052aca-80eb-4b3e-aea6-f0a844e7117a)
![precision-recall-scatter-3-undersam](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/1f2cb252-4cfe-46a6-97b3-25f5bdba3fa3)

### Final Optimization of Random Forest Model:
**The Random Forest Model performed the best and is the model chose to optimize.**
![cm-heat-randomforest-4-op](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/368abbba-b4f2-429d-a838-6e262f35b8c9)
![scatter-comparison-all-rf-models](https://github.com/leeangel0428/Project-3-Group-2/assets/137225965/6c7775c4-8118-4517-93e2-6e783edf662a)


## Resources (In Usage Order):

Aside from the sources cited below, everything used was retained information gathered from classes and class activities. As always shout out to our bootcamp TAs Sam and Randy for all their help answering our questions during office hours and our instructor Hunter for always being clear in his articulation of the course material.

**Dataset:**

Maharshipandya. (n.d.). Email Spam Dataset (Extended). Kaggle. Retrieved from: https://www.kaggle.com/datasets/maharshipandya/email-spam-dataset-extended

Spam Assassin’s Old Public Corpus. (n.d.). Index of/old/publiccorpus. Apache Software Foundation. Retrieved from: https://spamassassin.apache.org/old/publiccorpus/ 

**Cleaning:**

Maharshipandya. (n.d.). Email Spam Classification [98%]. Kaggle. Retrieved from:https://www.kaggle.com/code/maharshipandya/email-spam-classification-98

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

