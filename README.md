# Melanoma Detection Assignment

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

## General Information
- General information about the project:
  This project is to build a CNN based model which can accurately detect melanoma.
- Background of the project:
  Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- The dataset that is being used:
  The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following 9 diseases:

Actinic keratosis,
Basal cell carcinoma,
Dermatofibroma,
Melanoma,
Nevus,
Pigmented benign keratosis,
Seborrheic keratosis,
Squamous cell carcinoma,
Vascular lesion,

This means that the dataset contains 9 sub-sets in each train and test set. The 9 sub-sets contain images of 9 skin cancer diseases respectively.

## Conclusions
- With the given training dataset, the first training model has difficulties to identify the major patterns in the data and generalize on a new dataset. As a result, we decide to use data augmentation and add dropout to the model. Upon using the data augmentation and adding dropout, the model is less overfitting. Both the training and validation accuracy and loss are more aligned.
- There is class imbalance in the dataset where some classes have around 400 (such as "pigmented benign keratosis" and "basal cell carcinoma" samples while some classes have less than 100 samples (such as "dermatofibroma" with 95 samples and "seborrheic keratosis" with just 77 samples). For details:
dermatofibroma: 95 samples
melanoma: 438 samples
pigmented benign keratosis: 462 samples
basal cell carcinoma: 376 samples
squamous cell carcinoma: 181 samples
seborrheic keratosis: 77 samples
vascular lesion: 139 samples
nevus: 357 samples
actinic keratosis: 114 samples

Class has the least number of samples is 'seborrheic keratosis'
Classes dominate the data in terms proportionate number of samples are 'melanoma', 'pigmented benign keratosis', 'basal cell carcinoma', 'nevus'
- We rectify class imbalances present in the training dataset with Augmentor library. We are adding 500 samples per class to make sure that none of the classes are sparse. Then we use the Batch Normalization to create, compile and train the model again. The result showings that the overfitting becomes less than precious model. In addition, the training accuracy and loss are more aligned to the validation accuracy and loss (respectively). We get rid of overfitting. Class rebalance does help.
- The tutorial helps identifying melanoma through lesion images. The image analysis tools can help improve dermatologists' diagnostic accuracy.

## Technologies Used
- Github 
- Google Colab
- Matplotlib
- TensorFlow
- Keras
- Augmentor libraries

## Acknowledgements
Give credit here.
- This project was inspired by the dataset from International Skin Imaging Collaboration (ISIC).
- This project was based on [this tutorial]https://colab.research.google.com/drive/1wO9nzfUrSGp07qlAhmYpT8VrKfj5E_LD#scrollTo=LHodo28A4-NO


## Contact
Created by linhquetran - feel free to contact me!

