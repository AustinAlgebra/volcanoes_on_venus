# Volcanoes on Venus

This dataset contains images of the surface of Venus from Magellan's spacecraft circa 1990. The dataset labels some images as having volcanoes and others as no volcano. The images that contain volcanoes are also given a label for the type of volcano, radius, and number of volcanoes in the image.

I chose this dataset, because when I started at the University of Colorado Boulder, I was an astrophysics major. I later switched majors to mathematics, but I find astronomy very interesting and it was fun to be able to combine that interest with my data science learning. I also chose this as a challenge as I have not worked with image data before.

I now realize that the reason I have not worked with image data is that I have not learned all of the tools to best model it. This project will remain a work in progress that I come back to and tweak as I learn new skills.

Here's are my conclusions so far:

EDA:
For Exploratory Data Analysis, I had to fix the dataframes so that all of the pictures showed up and the image dataframes matched up with the labels. I found that there was class imbalance in the Volcanos? column that I was trying to predict. I created three different dataframes, one with the imbalanced, one with random undersampling, and one with SMOTE oversampling to compare in the different models.

Model Performance:
I found it counterintuitive that the Logistic Regression was more successful than Random Forest Classifier. I initially spent a lot of time trying to tune the Random Forest Classifier before even trying the Logistic Regression Classifier. This is a reminder not to just try my favorite model, or the one I'm most interested in practicing. I then tried to use GridSearchCV to find the best hyperparameters. The runtime on these was costly, which led to me not optimizing across all of the parameters. Still, I achieved nearly 100% recall and over 95% Accuracy, Precision, and F1.

Next Steps:
I would continue to try out different solvers and regularization algorithms to see if I can improve performance even more.

Takeaways:
I learned so much during this project. I learned a lot about class imbalance, including different sampling techniques, but also the problem of using accuracy as your only score for model performance. I was forced to go back to learning about different regularization techniques and their parameters. I started using cross_validate instead of cross_val_scores because of the problem of accuracy score. I started playing with GridSearchCV and will need to keep playing with it to find a way to reduce runtime to get the most out of it.
