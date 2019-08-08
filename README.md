# Image-Regression---Baseball-Players-Faces
Image Regression Problem

In MSA 8150(Machine Learning) class, a survey was done among students to evaluate what they thought about a person’s competency & trustworthiness when they examine their images. Facial images of baseball players were circulated among students & scores were collected. Later, a dataset was provided which contains results of the survey done to gauge “Competency” & “Trustworthy” score in MSA 8150 class. The definition of both the scores stands as follows:

• Competency Score: The average “competent" score MSA 8150 gave to a given image.
• Trustworthy Score: The average “trustworthy" score MSA 8150 gave to a given image.

# Problem Definition
The goal of this project is to see if machines can learn how human beings evaluate facial characteristics.
Data Information
The dataset provided contains a folder with 800 images of baseball players & an excel sheet containing respective scores – Competency & Trustworthy.
# Objectives and Constraints
• The dataset had a smaller number of images, so I decided to do image augmentation by performing image transformations like
o Rotations
o Zooming
o Horizontal/Vertical Flips
# Approach
The following is approach followed towards image regression problem. Since the dataset only contained 800 images, I have decided to increase the dataset using image augmentation techniques.
# Image Preprocessing and Augmentation
I have performed augmentation using two different approaches:
✓ Manual Augmentation (Using Open CV library)
✓ Automated Augmentation
o Automated augmentation was done using ImageDataGenerator function in Keras library of python programming language.
# Modeling
Two kinds of modeling were aimed to be performed - simultaneous regression and individual regression. In simultaneous regression, competency score and trustworthy score together as response variable are considered whereas in the individual regression, competency and trustworthy scores are considered as independent response variables. 

Additionally, two variants of modeling approaches were performed. The first one using Machine Learning algorithms and the other being Deep learning architectures .Different configurations of ImageDataGenerators were experimented as well. Finally K-fold cross validation was performed among different combinations of architectures to find the best model that showed least RMSE.

The model with least accuracy was submitted to test against unseen baseball player faces to predict the scores.

Acheived RMSE on Test Data - 1.92
