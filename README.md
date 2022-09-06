# Using machine learning to determine the success of a video game
What makes a blockbuster video game? An empirical analysis of US sales data.

## Dataset
- The dataset consists of one single csv file ("video_games.csv").
- The full description of the dataset is available at: <a href='https://corgis-edu.github.io//corgis/csv/video_games/'>github project page</a>.

# Machine Learning Pipeline


#### 1. The Dataset
- #### 1.1 Load the dataset
- #### 1.2 Dataset Analysis

#### 2. Classification
- #### 2.1 Preprocessing
- #### 2.2 Model Selection
- #### 2.3 Evaluation

#### 3. Summary

Machine learning uses artificial intelligence and statistical techniques to let computers to learn progressively to improve performance on a specific task with data with or without out being supervised.Depends on whether there is a learning feedback available, machine learning are typically classified into two broad categories supervised and unsupervised learning.Initially the dataset has 38 feature parameters. Our goal is to use these provided variables design a full fledged classification task on the Metrics.Review Score.We start with loading the data using the pandas or Numpy libraries.The length of the data is 1200 odd rows. I plotted different columns, there are three types of data fields categorical, boolean and numerical. I have dropped all the boolean columns because all of them were having the same value for all rows. 
We also dealt with Nan valure by using Imputaion. I dropped the highly correlated columns to decrease the unusual bias for a particular feature of the same type. Then I did the Target encoding of the categorical columns to create the dataset for the training of the model.The target reviews are being discretized into the 6 classes so that I can use those targets for the classification purpose. All of the feature values have been normalized to get the value between zero and one.The goal of normalization is to change the values of numeric columns in the dataset to use a common scale, without distorting differences in the ranges of values or losing information.Then i used the SMOTE library to remove the class imbalance, this helps to remove the biased and skewness of the known classes. Imbalanced classification is the problem of classification when there is an unequal distribution of classes in the training dataset.I used N- Fold Cross-validation to perform the analysis on one subset (called the training set), and validating the analysis on the other subset (called the validation set or testing set) and then build for models namely Decission tree, Random Forest , MLP and SV. AMong the four models I found out  that MLP and Random Forest are the best performing models on Cross Validatio, both with accuracy close to 70%.Then finally I decide to apply the MLP, which stands for Multi-layer Perceptron classifier which in the name itself connects to a Neural Network. Unlike other classification algorithms such as Support Vectors or Random Forest, MLPClassifier relies on an underlying Neural Network to perform the task of classification. it hasthe accuracy of nearly 36 to 40 for different iteration and parameters. It took nearly 2000 steps for the optimization to converge. Note:- Definitely by using different other techniques for encoding and rigorous hyperparameter tuning may increase the accuracy, but I also feel the size of the dataset is very small for this elementary task. I kept it to the use of one hot encoding which definitely is not the right choice, and if we can change the encoding that is definitely going to increase the accuracy.
