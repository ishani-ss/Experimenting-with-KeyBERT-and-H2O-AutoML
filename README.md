# Experimenting with KeyBERT and H2O AutoML
This repository captures experimentation with the keyword extraction algorithm KeyBERT, and the automatic predictive modelling and hyperparameter tuning interface H2O AutoML.


### Business Question: 
Can KeyBERT keyword extraction results be filtered by cosine similarity for better downstream modelling and to reduce the number of variables in small datasets (to prevent overfitting)?


### Further Notes:
* This project was undertaken to solve an workplace problem of overfitting NLP models using small datasets (<800 rows of data). The key issue was that keywords extracted from text would make up a column of the modelling dataframe, with columns exceeding the number of rows for the modelling data. This presented the risk of building overfit models, where more noise than actual signal may be registered by models by virtue of more features (columns of data), than samples available to learn from (rows of data).


### How to run the Code:
* The code uploaded to this repo can be run in the following order, with inputs and outputs available in the "Inputs" and "Outputs" folders uploaded to the repo.
  1. Run "101_data_preprocess.ipynb" to preprocess the modelling data
  2. Run "102_keybert_process.ipynb" to run KeyBERT on the modelling data (text)


### Data Folders:
* The "input" data folder contains the input datasets for the above Jupyter Notebooks.
* The "output" data folder contains the output files (in Excel format) for the above Jupyter Notebooks.
