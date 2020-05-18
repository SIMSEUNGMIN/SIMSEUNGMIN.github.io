---
title: "Summary of Stanford lecture"
data: 2020-05-19  
categories: mi333
---
  
This is Summary of Stanford lecture 1,2
[Summary_of_Stanford_lecture1,2.pptx](https://github.com/SIMSEUNGMIN/SIMSEUNGMIN.github.io/files/4647348/Summary_of_Stanford_lecture1.2.pptx)  
  
For humans, vision has become an important sensory system so that 50 percent of neurons are used for visual processing, and it makes many things possible, including survival, work and handling things.  
So the movement to study and computerize important visualizations for humans was natural.  
![image](https://user-images.githubusercontent.com/33623099/82267699-112def80-99a8-11ea-88bf-569eda8b6c93.png)  
  
Dividing objects is a method of clustering each pixel of an image in a meaningful direction.  
Using these methods, you may not be able to accurately recognize a person by collecting pixels, but at least you can identify the pixels in the background and the pixels that a person might belong to.  
![image](https://user-images.githubusercontent.com/33623099/82267804-5ce09900-99a8-11ea-9da8-aa526c0b067d.png)  
  
This method is called image segmentation, which allows us to extract the characteristics of the image.  
![image](https://user-images.githubusercontent.com/33623099/82267898-92858200-99a8-11ea-8e56-3a5006b48513.png)  
  
Through these studies, there are two goals for computer vision in the future.  
![image](https://user-images.githubusercontent.com/33623099/82267928-b1841400-99a8-11ea-9b13-d43230aedb0d.png)  
  
Solve these two goals, the company held a competition called ImageNet and developed an algorithm that improved accuracy by 10 percent in 2012.  
This algorithm is called CNN (Convolutional Network).  
![image](https://user-images.githubusercontent.com/33623099/82267964-c8c30180-99a8-11ea-9329-c651b7f4bd79.png)  
  
Classification of images in computer vision is an important task.  
But this becomes a very difficult problem for computers because images are only seen as a very large grid-shaped set.  
Even these parts need to be addressed by algorithms because pixel values change all by below.  
![image](https://user-images.githubusercontent.com/33623099/82268045-fdcf5400-99a8-11ea-941c-ab980e878b36.png)  
  
Instead of creating a rule set for an object, this data-driven approach begins by accessing the Internet and collecting a lot of data about the object.  
And we collect these data and use machine learning to learn.  
At this time, machine learning makes models that can recognize various objects by summarizing the data well.  
And test new images with learning models.  
![image](https://user-images.githubusercontent.com/33623099/82268151-40912c00-99a9-11ea-9684-e02324e17d6e.png)  
  
There are two functions.  
There is a downside to this classifier: it takes longer test time than training time.  
Because in actual use, the train time is not a problem even if it takes a long time, but it should work quickly at the test time.  
![image](https://user-images.githubusercontent.com/33623099/82268259-851cc780-99a9-11ea-9067-7741bc5701b1.png)  
  
And noise exists in Nearest Neighbor, and K-Nearest Neighbors was introduced to solve this problem.  
![image](https://user-images.githubusercontent.com/33623099/82268363-c6ad7280-99a9-11ea-93ae-f85770620518.png)  
  
In NN, there are K and distance that must be set directly, which are called hyper parameters.  
This two things is described as problem-dependent.  
![image](https://user-images.githubusercontent.com/33623099/82268419-e6449b00-99a9-11ea-9266-077c8df1eaff.png)  
  
If the input is an image, the K-NN classifier is not used well.  
There are two reasons.  
The first is that K-nn's test time is too slow.  
And the second is that the L1/L2 distance is not appropriate for measuring the distance between images.  
![image](https://user-images.githubusercontent.com/33623099/82268492-1724d000-99aa-11ea-810e-12d2aed12469.png)  
  
Linear classifier is based on CNN(Convolutional Neural Network) and NN(Neural Network).  
Linear Classifier is the simplest form of parametric model.  
There are two elements in the parametric model: one input image and one weight.  
You can think about how to combine weight W and input data in this way, which is the process of designing NN.  
Among these processes, multiplying input data X by weight W is called linear classifier.  
![image](https://user-images.githubusercontent.com/33623099/82268606-6408a680-99aa-11ea-8034-e29d505dff9c.png)  
 









