---
title: "Summary of stanford lecture 3"
data: 2020-05-22 
categories: mi333
---  
  
This is Summary of CNN lecture  
[Summary_of_Stanford_lecture3.pptx](https://github.com/SIMSEUNGMIN/SIMSEUNGMIN.github.io/files/4665282/Summary_of_Stanford_lecture3.pptx)  
  
The role of the loss function is to quantify how bad a random matrix W has.  
And our goal is to find the least bad W for every possible number of cases of matrix W.  
The input of the loss function is the predictive function F and the correct value Y.  
![image](https://user-images.githubusercontent.com/33623099/82616147-5e5bcc80-9c07-11ea-91ff-b356b6965fe3.png)  
  
An example of a loss function is multi-class Support Vector Machine (SVM).  
This is a generalized form of binary SVM to address multiple classes.  
It is also very suitable for image classification.  
![image](https://user-images.githubusercontent.com/33623099/82616209-8ba87a80-9c07-11ea-9c49-4a5ddb396056.png)  
  
The final Loss of the entire training set is the average of each training image Loss.  
![image](https://user-images.githubusercontent.com/33623099/82616354-e93cc700-9c07-11ea-89f1-235155c92315.png)  
  
If the loss function here is to tell the classifier which W we are looking for and which W we care about, there is a slight discrepancy here.  Because it is a contradiction to choose the Loss among the various Ws. Because this is like telling the classifier to find a W that fits the training data.  But in reality we don't care how much training data fits.   Our key is to use training data to find some sort of classifier because it will be applied to test data, not training data.   Therefore, we are not interested in the performance of training data, but in the performance of test data.  Therefore, if a classifier is asked to focus only on the loss of training data, it may have bad consequences.  For example, there is a data set of blue dots.   All we have to do at this time is fit those blue dots with some curve.   hen we will order the classifier to fit the training data and the classifier will create a curve to perfectly sort out all the training data.  However, this does not take into account the performance of the test data, so if the test data were to be received, the curve made earlier would be completely wrong.  Thus, to solve this, a method called Regularization is added, which adds one term to the loss function.  Thus, the loss function consists of two terms: in Data Loss term, the classifier is aligned with the training data, and in Regularization term, the model helps to choose a simpler W.   It also has a hyperparameter, lambda, which is responsible for the trade-off between the two sections.  
![image](https://user-images.githubusercontent.com/33623099/82616397-096c8600-9c08-11ea-9b79-e25925136bb9.png)  
  
We will apply softmax to this example.  
Previous SVMs used the score itself as Loss, but now they will exponentiate the score.  
When the exponentiation is complete, all values are positive.  
Then, regularize it so that the sum is 1.  
Once the normalization is complete, only the correct score is now given a –log value, which is called softmax.  
![image](https://user-images.githubusercontent.com/33623099/82616509-5a7c7a00-9c08-11ea-83e2-1966734a3410.png)  
  
The difference between the two loss functions is that the method of interpreting the scores is different to measure how bad they are.  
In the SVM, we cared about the margin between the correct score and the non-answer score.  
However, in softmax, probability is obtained and –log (correct answer class) is concerned.  
![image](https://user-images.githubusercontent.com/33623099/82616563-8e579f80-9c08-11ea-82f5-c5e5d7406b30.png)  
  
Five to ten years ago, when an image was inputted, it calculated various feature expression such as BOW and HOG and connected the calculated features to use the extracted vector as input to the linear classifier.  
When the feature is extracted once, the feature extractor does not change during classifier training.  
Only Linear classifier is trained during training.  
And it's similar to CNN.  
The only difference is that they try to learn features from the data rather than write them.  
Therefore, pixels go straight into CNN and create their own feature representation through multiple layers.  
And not only train the linear classifier, but also learn the entire weight at once.  
![image](https://user-images.githubusercontent.com/33623099/82616632-bcd57a80-9c08-11ea-96b5-82311082381d.png)










