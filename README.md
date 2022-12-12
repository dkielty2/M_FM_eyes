# Male_Female_Eyes_Classification

This repository contains a dataset of ~13,000 RGB images of human eyes sorted into the \female_eyes and \male_eyes folders. The dataset is open source and taken from Kaggle where it is called "Female and male eyes". See the Kaggle page for more details here [https://www.kaggle.com/datasets/pavelbiz/eyes-rtte?select=maleeyes].

In the analysis.py notebook, we classify images of human eyes as male or female. We train a binary logistic regression model using a 90/10 training/testing split and a L2 regularization penalty. The feature vectors are the pixel values at a given position and RGB layer of the image. The model is stored as model.sav via the Pickle Python package.

We also run the regression on grayscale 2D arrays. Training and fine tuning the logistic regression model on each and computing the accuracy of the model on the test set gives a prediction accuracy of roughly 80% for the grayscale images and 86% for the RGB images. 

Finally, we use the model to predict the gender of a small number celebrities. The eyes were manually extracted from headshots of celebrities found on the web. These headshots are stored in the \Celebs folder.
