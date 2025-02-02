# Experimenting with KeyBERT and H2O AutoML
This repository captures experimentation with the keyword extraction algorithm [KeyBERT](https://github.com/MaartenGr/KeyBERT), and the automatic predictive modelling and hyperparameter tuning interface [H2O AutoML](https://github.com/h2oai/h2o-3).

<br> 

### Business Question: 
Can KeyBERT keyword extraction results be filtered by cosine similarity for better downstream modelling and to reduce the number of variables in small datasets (to prevent overfitting)?

<br> 

### Further Notes:
* This project was undertaken to solve a workplace problem of overfitting NLP models of small text datasets (<800 rows of data). The key issue was that keywords extracted from text would make up a column of the modelling dataframe, with columns exceeding the number of rows for the modelling data. This presented the risk of building overfit models, where more noise than actual signal may be registered by models by virtue of more features (columns of data), than samples available to learn from (rows of data).

<br> 

### How to run the Code:
* The code uploaded to this repo can be run in the following order.
  1. Run "101_data_preprocess.ipynb" to preprocess the modelling data
  2. Run "102_keybert_process.ipynb" to run KeyBERT on the preprocessed modelling data (text)
