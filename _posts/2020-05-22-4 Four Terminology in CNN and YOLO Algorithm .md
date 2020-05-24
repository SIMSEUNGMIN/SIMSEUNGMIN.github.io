---
title: "4 concepts in CNN and operating YOLO algorithm"
data: 2020-05-22  
categories: mi333
---  
  
<h3>1. 1x1 convoltion</h3>
It has three advantages.  
First, Channel control.  
Second, Decreaing calculation.  
Third, Nonlinearity.  
  
A 1x1 solution is a filter that has a size of 1x1. 
This can control the number of channels, and for input image X, the channel of output Y is affected by the number of matrix W. 
Therefore, the number of channels can be adjusted by the number of 1x1 connections.  
  
![image](https://user-images.githubusercontent.com/33623099/82676391-488aed80-9c81-11ea-98df-1a9f92a35ada.png)  
  
If the number of channels can be adjusted here, the amount of calculation can also be reduced or increased, 
so it is also possible to reduce the amount of calculation.  
  
![image](https://user-images.githubusercontent.com/33623099/82676476-6b1d0680-9c81-11ea-86f5-8133885d812f.png)  
  
Finally, nonlinearity consists of several 1x1 Convs, given the structure of the Insertion. If you continue to use the Relu, the nonlinearity increases.  
  
<h3>2. Localization</h3>  
  
![image](https://user-images.githubusercontent.com/33623099/82676577-99024b00-9c81-11ea-8190-00d8c20eeb11.png)  
  
Localization, like the second image, is a model that outputs location information on the object in a given image, and mainly uses a bounding box. 
At this time, the bounding box prints the left top or right botom coordinates instead of the four vertex pixels.  
  
<h3>3. Sliding Window</h3>  
  
![image](https://user-images.githubusercontent.com/33623099/82676822-f5656a80-9c81-11ea-8b27-bd7a156bddff.png)  
![image](https://user-images.githubusercontent.com/33623099/82676841-feeed280-9c81-11ea-98ac-76e3a7232714.png)  
  
Sliding Window is an brute force idea. 
This method divided an input image to small sections and scan all sections to find object. 
An example, here is picture with 8 in the center. 
At this time, we want to find the section that includes 8. 
Therefore, first, we divided an image to small sections and scan all sections at once. 
Finding 8 in this way is called sliding window. Some limited cases work well but this algorithm actually very inefficient because the size of the sections being divided must be varied and checked several times.  
  
<h3>4. YOLO</h3>  
  
![image](https://user-images.githubusercontent.com/33623099/82678047-e7b0e480-9c83-11ea-9379-31eb2c5c4802.png)  
  
YOLO is a single-step object detection algorithm. YOLO Algorithm divides images into grids of the same size. 
Then the number of bounding boxes is estimated based on the predefined anchor boxes for each grid. 
At this time, Calculate the reliability of each of the several expected bounding boxes, then leave the high-reliability bounding boxes aside and suppress the low-reliability bounding boxes near them.  
This algorithm has two advantages.  
First, It is a simple process and it's very fast.
Second, There is a high contextual understanding of class by viewing the entire image at once. As a result, it shows a low background error (False-Positive) error.
  
  
  
  
Finally, I successed execution of YOLO algorithm...  

This is result of execution.
  
![result](https://user-images.githubusercontent.com/33623099/82760493-c5a79580-9e2e-11ea-8cac-3da51a442147.jpg)  
  
It is definitely faster than other algorithms, but the accuracy seems to be a little lower.  






