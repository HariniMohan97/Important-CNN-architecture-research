# Session-3

Aim:- The assignment was to build a CNN with less than 20k parameters and achieve a validation accuracy of 99.4% and above on mnist dataset.

In the network I built, I kept the following things in mind:

1) Since the image size is 28x28, and mnist is a comparatively easy dataset, I used fewer number of kernels in most layers. This also allowed me to maintain lower number of parameters.

2) I incorporated 1x1 kernels to reduce the number of parameters as well. 

3) Using Batch normalisation really helped in improving the accuracy. It basially normalises the output of every layer before it goes onto the next layer.

4) The batch size is basically the number of batch propagations that occurs. So increasing it also helped in increasing accuracy. Although I kept it at 32 at the end to push the network. 
So this is the first thing I tried along with removing the relu activation function from the last convolution layer.

5)The model was definitely overfitting, i.e, the training accuracy was much higher than the validation accuracy. This was addressed by the usage of drop out. Drop out forces the network to learn the more robust features that are required. Although Dropout doubles the number of iterations required to converge.

6) Scheduling Learning Rate also helped in converging faster or reaching the minima sooner. Keeping a smaller lr as we get closer to the minima helps in converging faster.

7) I also followedother helpful rules like, having maxpooling layer after atleast 2-3 convolution layers and far away from the last output layer. I made sure that the receptive field was close to 28x28. 26x26 or 24x24 would also be sufficient since the numbers are small and a smaller RF would be enough to see them. 

You can go through my code. My code has comments for every cell for better understanding.
