# Data Science Predict user ratings (1 to 5) for the review
* Predicting user ratings by given product reviews.
* Explored about 150000 product reviews.
* Processed text: lemmatize text, removing special characters, removing sxtra whitespace, removeing stopwords.
* Optimized the system by using Binary classification model(Logistic regression, SVM), and Neural Network(DNN, LSTM, LSTM with word embeddubg).

## Code and Resources Used
**Python Version:** 3.7  
**Packages:** pandas, numpy, spacy, nltk, sklearn, keras  
**Problem statement and Data:** https://www.kaggle.com/davydev/shopee-code-league-20/tasks?taskId=1571  
**text-preprocess reference:** https://github.com/dipanjanS/text-analytics-with-python  
**model reference:** https://github.com/emmanuellaanggi/disaster_tweet_sentiment/blob/master/(Medium)_Text_Classification_Disaster_Tweet_.ipynb    

## Text Pre-process
Doing text preprocess:
* Remove accented characters
* Expand contractions
* Lowercase the text 
* Remove extra newlines
* Insert spaces between special characters to isolate them
* Lemmatize text
* Remove special characters
* Remove stopwords
* Tokenize   

## Model Building
I tried five different models and evaluated them using Accuracy and confusion matrix: 
Fitting the data from simple model to complexity model
* **Logistic Regression** - Baseline for the model
* **SVM** - More complexity model
* **DNN** - Using Neural Network  
  ![alt text](https://github.com/ILing82816/Product_review/blob/master/dmm_model.png) 
* **LSTM** - Considering the text order, try to use LSTM  
  ![alt text](https://github.com/ILing82816/Product_review/blob/master/lstm_model.png) 
* **LSTM + FastText** -  Add word embedding  
  ![alt text](https://github.com/ILing82816/Product_review/blob/master/lstm_em_model.png)

## Model performance
The LSTM + FastText model far outperformed the other approaches on the test and validation sets.
* **LSTM + FastText:** Accuracy = 0.4807  
* **Logistic regression:** Accuracy = 0.2804 
* **DNN:** Accuracy = 0.4497 
* **LSTM:** Accuracy = 0.4549    

