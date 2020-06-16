# stream_project

## Basic Algorithm Introduction

The paper introduced an innovative coding method for image classification called Locality-constrained Linear Coding (LLC). Image classification is perhaps the most important part of digital image analysis, by which a machine could technically “see” the world. Image classification helps us better analysis and organize the digital graphic information and extracts useful intelligence that could be beneficial to people’s life.

Firstly, I obtain graphic information by translating each feature point on an image into a feature vector called descriptor via SIFT algorithm. Intuitively we can think of descriptors as digital representation of the image’s graphic features. Some elementary image classification methods compare descriptors directly, which turns out to be inaccurate. In a more advanced SPM algorithm, the descriptor matrix goes through the coding process in which each descriptor vector gets codified into a code vector. Usually a codebook is utilized in the coding process, which might be intuitively deemed as a “book” of general features. We approximate each descriptor with a linear combination of column vectors in the codebook and use the vector of coefficient (usually weight coefficients) as the code for the descriptor. Intuitively one can imagine this process as using the general features in the codebook to represent an original feature in the image and record the features we used.

After that, we have stored the feature in a feature folder and use it as training data. For training, I have used kmeans cluster with svm. By doing this, I have reached the good accuracy. 

## Process to reproduced the result again.
1- open the project folder in octave/matlab.

2- Run the extr_sift.m script in octave/matlab to apply SIFT descriptor, which will be stored in data folder.
  so we have data with SIFT descriptor.
  
3- Now we have LLC_test.ipynb, We have to open it into Jupyter Notebook to run this code.
   After opening the file, we need to run every cell of notebook. After running the last cell, we can see that training      started and we have to wait till training and we can see the result.
  
  
  ## Result:

Average classification accuracy:  94.83%

Standard deviation in accuracy:  2.17%
