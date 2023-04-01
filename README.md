# Web Page Phishing Detection Model

## Introduction
This project builds a machine learning model to predict whether a web page is legitimate or a phishing page. The dataset used in this project is the [Web Page Phishing Detection Dataset](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset).

## Getting Started
To get started with this project, clone the repository and install the necessary dependencies by running the following command:


## Dataset
The dataset used in this project contains the following columns:
- `url`: the URL of the webpage
- `nb_dots`: the number of dots in the URL
- `nb_hyphens`: the number of hyphens in the URL
- `nb_at`: the number of @ symbols in the URL
- `nb_qm`: the number of question marks in the URL
- `nb_and`: the number of ampersands in the URL
- `nb_eq`: the number of equal signs in the URL
- `nb_underscore`: the number of underscores in the URL
- `nb_tilde`: the number of tildes in the URL
- `nb_percent`: the number of percent signs in the URL
- `nb_slash`: the number of slashes in the URL
- `nb_star`: the number of asterisks in the URL
- `nb_colon`: the number of colons in the URL
- `nb_comma`: the number of commas in the URL
- `nb_semicolumn`: the number of semicolons in the URL
- `nb_dollar`: the number of dollar signs in the URL
- `nb_space`: the number of spaces in the URL
- `nb_www`: the number of "www" in the URL
- `nb_com`: the number of ".com" in the URL
- `nb_dslash`: the number of double slashes in the URL
- `http_in_path`: whether "http" appears in the path of the URL
- `https_token`: whether "https" appears in the URL
- `domain_length`: the length of the domain name
- `path_length`: the length of the path in the URL
- `subdir_length`: the length of the sub-directory in the URL
- `domain_in_path`: whether the domain name appears in the path of the URL
- `domain_token`: whether the domain name appears as a token in the URL
- `www_token`: whether "www" appears as a token in the URL
- `path_token`: whether the path appears as a token in the URL
- `num_vars`: the number of variables in the URL
- `num_subdomains`: the number of sub-domains in the URL
- `ssl_state`: whether SSL is used in the URL
- `long_url`: whether the URL is long
- `age_of_domain`: the age of the domain
- `ip`: whether the URL contains an IP address
- `label`: whether the URL is legitimate or a phishing page

## Feature Selection
Features were selected based on their correlation with the target variable. The selected features were:
- `nb_dots`
- `nb_hyphens`
- `nb_at`
- `nb_qm`
- `nb_and`
- `nb_eq`
- `nb_slash`
- `nb_percent`
- `nb_star`
- `nb_colon`
- `nb_comma`
- `nb_semicolumn`
- `nb_dollar`
- `nb_space`
- `nb_www`
- `domain_registration_length`
- `domain_age`

## Preprocessing
### Setup Predictors and Targets
The selected features were used as predictors and the `status` column was used as the target variable. 

### Train-Test Split
The dataset was split into training and test sets using a 80:20 split ratio.

## Model Fitting and Evaluation
Four models were fit on the training data and evaluated on the test data using accuracy and confusion matrix. The models used were:
- Logistic Regression
- Support Vector Machine
- Naive Bayes
- Decision Tree

The accuracies of the models on the test data were:
- Logistic Regression Accuracy: 0.8736
- Support Vector Machine Accuracy: 0.7213
- Naive Bayes Accuracy: 0.8005
- Decision Tree Accuracy: 0.9274

Based on the results, it can be concluded that the logistic regression and support vector machine models performed the best in predicting whether a webpage is legitimate or a phishing page.
