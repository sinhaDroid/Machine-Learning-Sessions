# Article on Epochs and 1x1 convolution by Nidhi Sharma from Batch 4

# 1) Epochs:
One Epoch means going over the all the samples in your training set once i.e one forward and backward pass of all the training set examples. It may take several iterations to complete one epoch since the data is usually divided into batches. Also it may take hundreds of epochs for your algorithm to converge as gradient descent updates the weights of the network by a small amount and only 1 epoch won't be sufficient for convergence.
![alt text](https://image.slidesharecdn.com/publishdeeplearninghandson-150819055326-lva1-app6891/95/handson-deep-learning-in-python-13-638.jpg?cb=1445114490=)

# 2) 1x1 convolutions
It is basically convolution with filter of size 1x1. It is used for dimensionality reduction & makes no sense if the previous layer has only one feature map/channel. It is nothing but pixel-wise weighted sum across all the channels of the previous layer for that particular pixel. It introduces non-linearity into the network as 1x1 convolution is equivalent to matrix multiplication which makes the model look deeper and increases the number of parameters.
![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7ZBI81pcaluI6nlRHyyE7GraMpTO5TNYKHG1K9FCRPqCl0wEm)
