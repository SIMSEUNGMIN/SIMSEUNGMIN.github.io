---
title: "Summary of stanford lecture 6"
data: 2020-05-29 
categories: mi333
---  
  
This is PPT about Summary of CNN lecture  
[Summary_of_Stanford_lecture6.pptx](https://github.com/SIMSEUNGMIN/SIMSEUNGMIN.github.io/files/4698722/Summary_of_Stanford_lecture6.pptx)  
  
This is six types of activation function.  
![image](https://user-images.githubusercontent.com/33623099/83202649-febf6d00-a182-11ea-867f-6c1ad0529611.png)  
  
This is the sigmoid.  
The sigmoid function is as we have up here, one over one plus e to the negative x.  
And what this does is it takes each number that's input into the sigmoid, so each element, and the elementwise squashes these into this range [0,1] right.  
But there’s three problems.  
First problem is saturated neurons kill the gradients.  
Second problem is sigmoid outputs are not zero-centered.  
And then third problem is an exponential function is a little bit computationally expensive.  
![image](https://user-images.githubusercontent.com/33623099/83202700-21518600-a183-11ea-9bff-f0b4974a8966.png)  
  
This is the tanh.  
This looks very similar to the sigmoid, but it ranges from –1 to 1 and the main difference is that it's now zero-centered.  
This function solves a second problem but it kills gradients when is’s saturated.  
Because this function has still these regimes where the gradient is essentially flat.  
![image](https://user-images.githubusercontent.com/33623099/83202798-5a89f600-a183-11ea-844c-c40a30912489.png)  
  
This is the ReLU.  
It takes an elementwise operation on your input and basically, if your input is negative, it's going to put it to zero.  
And then if it's positive, it's going to be just passed through.  
And so this is one that's pretty commonly used, it doesn't saturate in the positive region.  
So there's whole half of our input space where it's not going to saturate, so this is a big advantage.  
However a problem with the ReLU, is that it's still not zero-centered.  
In the positive half of the inputs, it doesn't have saturation, but this is not the case of the negative half.  
And we can also get this phenomenon of dead ReLUs.  
![image](https://user-images.githubusercontent.com/33623099/83202918-8dcc8500-a183-11ea-9a58-71f0ac9b7771.png)  
  
A dead ReLU occurs when the ReLU is away from the data cloud in this data cloud consisting of training data.  
Dead Relu will never activate and never update.  
![image](https://user-images.githubusercontent.com/33623099/83203253-02072880-a184-11ea-9fcd-d8611c7f02b1.png)  
  
This is the leayky ReLu.  
This looks very similar to the ReLU, but is no longer zero in the negative regime.  
we're going to give a slight negative slope here And so this solves a lot of the problems that we mentioned earlier.  
And no Dead Relu.  
![image](https://user-images.githubusercontent.com/33623099/83203217-e865e100-a183-11ea-875e-38b7bb997d9e.png)  
  
This is Exponential Linerar Unit, ELU.  
This has an output value close to zero-mean while retaining the advantages of the RELU.  
However, compared to leaky Relu, the ELU has saturation at negative.  
At this time, ELU believes that this kind of saturation makes stronger from noise.  
![image](https://user-images.githubusercontent.com/33623099/83203388-485c8780-a184-11ea-8154-c232dc12cc46.png)  
  
There are two ways to zero-center an image.  
The first is to subtract the average value of the image before the input image enters the network.  
The second is to calculate the mean independently for each channel and subtract before the input image enters the network.  
We usually use first way.  
![image](https://user-images.githubusercontent.com/33623099/83203458-70e48180-a184-11ea-9665-13eddfd8a4d8.png)  
  
Use Xavier initialization to solve the weight initialization problem.  
This xavier initialization is the balancing of I/O distribution.  
But it doesn't work well in Relu.  
![image](https://user-images.githubusercontent.com/33623099/83203525-95d8f480-a184-11ea-803a-c52e045be6a8.png)  
  
Because Relu makes half of the output zero, the variance of the output is halved.  
In order to solve this problem, we will distribute 2 to the value of the weight.  
![image](https://user-images.githubusercontent.com/33623099/83203600-c02ab200-a184-11ea-88b4-5292e10c08d5.png)  
  
This is batch normalization.  
This is one of the ways to maintain activation in the Gaussian range.  
And this is usually inserted after fully connected or convolutional layers.  
What normalization does is force the input to exist only in a lineal area.  
This eliminates any saturation, and by adding two hyper parameters, you can control saturation.  
If you look at the expression, we're going to scale by some constant gamma, and then shift by another factor of beta.  
![image](https://user-images.githubusercontent.com/33623099/83203656-dfc1da80-a184-11ea-8d63-f0d2493950df.png)  
  
The Learning rate is one of the first hyper parameters to be determined.  
Cross-validation is one of the ways you can optimize hyper parameters and choose the best of them.  
First, perform a coarse stage.  
Coarse stage selects the value from a wide range and checks if the current value works well.  
In the second fine stage, try to set a narrower range and make the learning longer to find the best value.  
![image](https://user-images.githubusercontent.com/33623099/83203839-519a2400-a185-11ea-943f-d4529b7e1a5f.png)  
  
Another way to find hyper parameters is to use grid search.  
Sampling hyper parameters at fixed values and intervals.  
But in reality, it's better to do a random search like before than a grid search.  
Random search is better because it's more sensitive than Grid Search.  
![image](https://user-images.githubusercontent.com/33623099/83204003-ae95da00-a185-11ea-9a51-53e998522cd2.png)  










