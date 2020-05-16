---
title: "Summary of CNN"
data: 2020-05-15 
categories: mi333
---
  
This is Summary of CNN lecture
[Summary_of_CNN_SeungminSim.pptx](https://github.com/someonewho/someonewho.github.io/files/4631368/Summary_of_CNN_SeungminSim.pptx)  
  
CNN(Convolution Neural Network) is a type of artificial neural network used for image recognition and processing.  
It is designed to process pixel data because the existing fully connected layer use only one demension as input data.  
![image](https://user-images.githubusercontent.com/33623099/82106465-20b8f880-975c-11ea-8c72-71f792cfba97.png)  
  
The following is characteristic of the CNN.  
1. Maintain I/O data geometry for each layer.  
2. Preserve image space information, effectively recognize features with adjacent images.  
3. Extract and learn characteristics of images with multiple filters.  
4. A pooling layer exists that collects and strengthens the characteristics of the extracted images.  
5. Since filters are used as shared parameters, there are fewer learning parameters compared to normal artificial neural networks.  
  
This is example of CNN, CNN is composed of convolution layer, pooling layer and fully connected layer.
![image](https://user-images.githubusercontent.com/33623099/82106659-61654180-975d-11ea-8849-d474fa90aea9.png)  
  
This is types of CNN models.
- ReNet-5  
- AlexNet  
- VGG-16  
- ResNet  
- Inception  
  
ResNet is designed to overcome the degradation of performance as the layer gets deeper.  
The cause of this problem is Gradient Vanishing.  
![image](https://user-images.githubusercontent.com/33623099/82106809-5363f080-975e-11ea-8d4d-e85ea7fc4422.png)  
  
Inception is a model that solves the problem of computation when you want to combine results by applying mulitple filters and pooling to input data ar once. This model performs multiple filter and pooling calculations at once, but uses 1x1 convolution to reduce the number of channels in each input data for reducing calculation. And this picture is Inception network. There are two things to pay attention to. First is we do not use this module close to the input because this module is not effective if it is close to the input. because the closer it is to the input, the less effective it is. Second, the softmax results are not only at the end, but in the middle. Because this network is a very deep network, there can be a Gradient vanishing.  
![image](https://user-images.githubusercontent.com/33623099/82106956-27953a80-975f-11ea-939b-73d4c45b02c9.png)  
  
YOLO divides input data into a grid to determine the class at once and incorporates it to distinguish the final object. So the video is fast enough to work almost in real time. YOLO first divides input data into girds and then applies classification & localization. And then the bounding box is drawn based on the square in which the center point of the object is located. At this time, several bounding boxes may appear, and we use the IOU function to remove the bounding boxes except the one whth the highest accuracy. All of these processes are carried out as many as the number of anchor boxes, and only the final bounding box remains when these courses are completed.  
![image](https://user-images.githubusercontent.com/33623099/82107204-cff7ce80-9760-11ea-8979-0b5cb0e9852c.png)







