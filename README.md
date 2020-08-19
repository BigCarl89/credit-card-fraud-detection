# Credit Card Fraud Detection by Alberto Carlone
#### Udacity Data Scientist Nanodegree

### Project Description
This is the final project of Udacity Data Scientist Nanodegree, based on Kaggle dataset Credit Card Fraud Detection.  
The dataset can be found at this [link](https://www.kaggle.com/mlg-ulb/creditcardfraud).  
Our aim is to build a model through Machine Learning that can predict if a transaction is fraudolent or not, taking into account that we also have to reduce false positive (in the form of service interrutption for our customers).  
To achieve this, we also have to address the problem of the unbalanced data with oversampling algorithms.

### Libraries and Python Version
- Python 3.7.5
- Pandas, Numpy
- Seaborn, Matplotlib for Visualizations
- Scikit-learn for Machine Learning
- Imbalanced-learn for oversampling algorithms and pipelines
- Time for custom timing functions used during model fitting

### Installing libraries
To install imblearn follow this [guide](https://imbalanced-learn.readthedocs.io/en/stable/install.html)
If you are using Anaconda, the rest of the libraries are already present.

### Files description
In this repository is present the Jupiter Notebook in .ipynb and in HTML and this README file. The dataset is not present since it is available directly from Kaggle.

### Results Summary
Oversampling was made through ADASYN algorithm. With the dataset balanced i have then proceded to fit, and subsequently tune with GridSearchCV, a Random Forest Classifier (and also a Logistic Regression Classifier but with worse results) obtaining already good results:
- Precision 0.83
- Recall 0.87
- Fall-out 0.000293
- F1-Score 0.85  
  
These result can be improved tuning the probability threshold of a transaction to be fraudolent or not. I have then graphically located which Precision/Recall scores are suited for a good balance of values and then, through similarities between our generated arrays of Precision and Recall, find the best values of thresholds to consider.  
  
In the end, using a threshold of 0.71 with Random Forest Classifier, i have improved the results with the following scores:
- Precision 0.91
- Recall 0.86
- Fall-out 0.000141
- F1-Score 0.88  
  
### Deliverables
Other than this repo, a blog post is made available on Medium at this link

## Authors

- [**Alberto Carlone**](https://github.com/BigCarl89)


## Acknowledgments

- Machine Learning Group - ULB for providing the dataset on Kaggle
- Imbalanced-learn creators for making an awesome library

