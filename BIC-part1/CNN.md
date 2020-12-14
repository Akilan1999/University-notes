# CNN 

## What is a CNN? 
In deep learning, a convolutional neural network (CNN, or ConvNet) is a class of deep neural networks, most commonly applied to analyzing visual imagery. They are also known as shift invariant or space invariant artificial neural networks (SIANN), based on their shared-weights architecture and translation invariance characteristics. They have applications in image and video recognition, recommender systems, image classification, medical image analysis, natural language processing,brain-computer interfaces, and financial time series.

## Convolution operation (LeNet 5)
Comparison patch by patch. Use backproprogation to figure out features.

- Line up the feature and the image patch.
- Multiply each image pixel by the corresponding feature pixel.
- Add them up.
- Divide by the total number of pixels in the feature.

If the output is 1 then it is a match and does the sliding window approach. Do comparion of patch for all patchtes separately.
Using this approach we can create a more sparse neural network. Easier to do gardient decent (back propogation)
Multiple convolution operations can be done before polling.

## Polling: shrinking the image stack
- Shrink image stack
- Pick window slide 
- Pick a stride 
- Walk window through filtered images 
- For each window take maximum value 

We get max pooling which is a dimentionality reduction 

## Normalization 
- ensures math doesn't break when doing back propogation (i.e change negative to 0 else stays the same we call this the ReLU activation function)

## Steps 
- Convolution 
- polling 
- ReLU
(order can be swapped)

## Flatten the final multi dimentional array and feed it into a traditional neural network 

## learning 
- Features in convolution layer 
- Voting weights in fully connected layers 
- (A) -> backpropogation 

## Hyper parameter

### Convolution 
- No of features 
- Size of features 

### Polling 
- Window size 
- Window stride 

### Fully connected 
- No of neurons 

## Architecture (Swarm intelligence is used)
- How many of each type of layer 
- What order 

## Applications 
- Can also be used to make videos (just extra dimention called time) 

## Limitation 
- Only capture local special patterns 
- If you main output stays the same even after swapping coulmns (No point using CNN)

## CNN is for finding patterns and using them to classify iamges 





