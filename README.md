# Portfolio projects

In this repository, it contains several data science projects I did before. The topics of my projects including regression model, classification model, NLP(natrual language peocess), and neural network. In each jupyter notebook, you can see every step for a data science project, including import data, data preprocessing, EDA, data engineering, fit model, and model validation.

1. House Sale Price Prediction
2. March Machine Learning Mania 2017

* For this project, I was trying to build a model to predict the outcomes of 2017 US men's college basketball tournament. The datasets were downloaded from Kaggle competition. There were eight different datasets, which were regular season compact result, regular season detailed results, tourney compact results, tourney detailed results, tourney seeds, tourney slots, seasons, and teams.
* The target for the prediction is binary which is winning or losing, and 1 stands for win and 0 stands for lose. The features I used to build the model were seeds number of tournament, number of winning games of last tournament, and the performance of regular season. The data I used to train model was from 2003 to 2016.
** The process to create a new dataset to fit in the model: 
  * Create a dataset with calculating the mean regular season’s statistics and choose the features which have more than 0.05 correlation value with result. 
  * Create a dataset with the total number of winning games from las tourney of each team. 
  * Create a dataset with numeric seed value for each team. 
  * Create the dataset with winning teams, winning teams’ features, losing teams, and losing teams’ features by merge the dataset created before. Calculate the difference between winning teams and losing teams. 
  * Create the final dataset with concat difference between winning teams and losing teams and  negative difference value, and create a target column with binary result 1 and 0.

* The algorithm used were Logistic Regression, SVM(Support Vector Machines), KNN(K-Nearest Neighbor), Decision Tree, Random Forest and Gradient Boosting.


3. Amazon Food Review NLP analysis project

* Amazon food review dataset has 568454 reviews and each review contains ten features which are Id, Product_Id, profile name, helpfulness numerator, helpfulness denominator, score, time, summary, and text. I chose the Id, score and summary features to do deep analysis.
* 1. Preprocessing text data including remove punctuation and numbers, lowercase letter, remove stop words, tokenization, and stem remaining words.
    2. Using TfidfVectorizer() transform text bag into DataFrame
    3. Reduce features and eliminate multicollinearity with using PCA(Principle Component Analysis) method.
    4. Visualization high frequency word (the most discrimination between documents) with using wordcloud package in Python.
    5. Using RandomForestClassifier, LogisticRegression, and Naive Bayes learning method to create classification models to predict positive or negative.
    6. Use LDA(Latent Dirichlet Allocation) to figure out ten topics of customer summary and find which summary is the most likely to belong to each topic.

4. CNN(Convolution Neural Network) image recognition 
* There are two projects focus on image recognition. One is dog breed identification, and the other is the hand writting digits identification. The data preprocessing for these two projects are similar.
* As the CNN model needs four dimension input data, I convert .jpg file into Numpy Array, which has four dimensions with using image package in Python. Those four dimensions are number of images, pixel value for width, pixel value for width, and RGB value.
* Adjust several CNN neural network variables, such as layers, epochs, learning rate and dropout rate to get better performance.
* I used cross-entropy loss value to evaluate model performance.
