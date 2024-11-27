# Convolutional Neural Network (CNN)
- It is a specialized deep learning system designed to handle visual data by capturing spatial dependencies and hierarchies of features, which are common in images. It diminishes 













---------------------------------------------------------------------------
Deep Learning
Convolutional Neural Networks
Convolution Operation:-
1st step is to extract features from the image
For this, we use filters to extract different features 
The sliding window algo will be used for comparing filter and image
Whenever the pattern of the filter is seen in the image, that is where the feature map will have the highest value.
Technically, cross-correlation is being performed. Convolution involves horizontal and vertical flipping of the filter. Flipping allows for the associativity property in some signal-processing applications. Not required in neural networks. So the term ‘convolution’ is used here by convention.

The network learns the weights of the filters to detect various features.
Example:-
There can be many types of vertical filters. So we need to learn the best filter that can be used.
					
Padding:-
Output size:- (n-f+1)*(n-f+1)
N is the size of image n*n and f is the size of filter f*f
Output shrinks
Corner/ edge pixels contribute less to the output 
Loss of information
Padding is usually done with zeros
P is the number of pixels added to the boundary of the image
Output size will be (n+2p-f+1)*(n+2p-f+1)
Valid and Same Convolutions:-
Valid convolution: no padding
Same convolution: padding done so that output size is same as input size
N+2p-f+1 = n
P = (f-1)/2
By convention, f is usually odd
The filter has a central pixel
Strided Convoution:-
Stride(s): Step size of sliding window
Output size: (((n+2p-f)/s)+1)*(((n+2p-f)/s)+1)
If not an integer, take floor value
Filter must lie entirely within the image


Convolution on RGB images:-
No. of channels in input = No. of channels in the filter.
Ex. of the filter is vertical edges in all channels are to be detected.
Multiple filters:- 
n*n*nc size of RGB image and f*f*nc where NC is no. of filters
Output size:- (n-f+1)*(n-f+1)*nf where nf is no. of filters


One Layer of Convolution Network:-
Number of parameters in a layer:-
Each filter:- f*f*nc*nf
Notation:-



Pooling:-
Reduce the size of representation to speed up the computation 
Makes detected features more robust
No parameters to learn
Input: nh*nw*nc
Output: (((nh-f)/s)+1)*(((nh-f)/s)+1)*nc
Each channel is handled independently
Types of pooling:-
Max pooling
Intuition for the max pool: The large number probably represents some feature
Avg Pooling

Convolution Neural Network
Convolution:- apply filters to generate feature maps
Apply non-linearity:- often ReLU
Pooling:- downscaling operation on each feature map
Train model with image data. Learn weights of filters in convolution layers
CNN for classification: Feature Learning
Learn features in input image through convolution
Introduce non-linearity through activation
Reduce dimensionality and preserve spatial invariance with pooling
CNN for classification: Class Probabilities
CONV and POOL layers output high-level features of the input
A fully connected layer uses these features for classifying input image
Express output as the probability of an image belonging to a particular class.


