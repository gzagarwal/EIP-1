GAURAV AGARWAL

BATCH3

EMAIL ID  : gaurav130403@gmail.com

#### Convolution

###### ---------------------------

Convolution is the extraction of third function from the two input functions , We can perform any function while doing convolution.Convolution can be done on the images as well.

Suppose we have color images of RGB channels so we have 3 channels, in the number and matrix format of 28x 28 and the second layer is the kernel of 26x26.

It used for blurring,edge detection and sharpening the image.It also means we can manipulate the pixels of the image.

We can convolve the image 

![img](http://colah.github.io/posts/2014-07-Understanding-Convolutions/img/RiverTrain-ImageConvDiagram.png)



#### Activation Functions

-------------------------------------

It helps the neural network to learn the complex and non linear network. This will calculate the sum of products of inputs and weights , On top of that we can apply any activation function . To recalculate weights while applying the back propagation activation function  

The range of that activation function , Like Sigmoid function in range from (0 to 1), Relu (0 to Infinity) and Leaky Relu (-Infinity to + Infinity) .It plays a pivotal role while calculating the gradient descent. If we don't have activation function then the gradient can be vanishing.

When we apply activation function as this is differentiable , then it will help to minimize the loss by recalculating the weights between the previous layer and the current layer , as it goes from output to Input layer in the backward direction.

![img](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/10/17123344/act.png)



#### Epoch

Number of time entire dataset runs with the training data, that is called Epoch.An epoch contains multiple batches , In one epoch we can run multiple batches to train the Parameters. 

One epoch cycle will be completed once we initialize the process , calculate the weight loss at the output layer , Now in return backpropagation start , we recalculate the weights and at the initial layer , recalculated weights will be updated , These will be the input for the next Epoch cycle.

Example , In a Sample of 5000 dataset , We ran 500 epoch with the batch size of 100 .Now we can have 500 batches to be ran for 100 batch size each in the total of 500 epoch. In total we can train total of 250000 batches with 500 epoch.



## Filters/Kernels

We apply filters on the image to extract the features while applying the convolution. Filters can be applied on Conv2D layer, filters are applied on 1 Grey Channel .It can also be applied on Conv3D layer , it means filters are applied on multiple channels, colored one as well.

Filters played the important role in the Convolution of the images . We can extract the features on image applying filters.

e.x. (3x3) size of filters to be applied on 10x10 , This will give in turn 8x8 size of the image .



##### 1x1 Convolution

----------------------

With 1x1 convolution we can achieve dimension reductionality in the network. Some unwanted features can be removed from the image. We will also optimize the computation on the model with 1x1 filter.

Suppose we have 100x100 x256 image and we convolve it with a set of N filters for the size of 1x1x256 , the number of features will be reduced from 256 to N . Resultant volume can 100x100xN

This replaces the fully connected layer.

if we apply 3x3 on 100x100x512 Image with D filters. That can be computationally expensive, We can replace 3x3 with 3x1 and 1x3 , the path can (3x1 to 1x3 to 3x3). This will reduce dimension reductionality.



