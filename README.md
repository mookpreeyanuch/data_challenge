# Image classification
Classifying hand-written digits using a Convolutional Neural Networks (CNN) in Tensorflow.

## Set up
This provides a requirements.txt for pip to install an environment.
```bash
$ pip install -r requirements.txt
```
## Dataset
The dataset contains 20,000 images of handwritten digits, 0 - 9. Each image is 28 x 28 pixels in size. It also includes labels for each example, a number indicating the actual digit (0 - 9) handwritten in that image.

In this project, We do a classic train/test split using 70% training and 30% testing

## Modeling and results
To make a prediction model, we use a simple Convolutional Neural Networks (CNN) with 3 layers following by Fully conected layer.
 
### Model
Convolutional Neural Networks (CNN) is a type of neural network which use the concept of convolution to find matched filter. The CNN learns the filters which will be used to convolved with the input signal (which is an input image in this case) and learn the best filters that will find a pattern. This type of neural network typically used together with Max Pooling Layer

### Max Pooling Layer
This layers allow the feature map (output from CNN) to be reduced in size. Which makes the later CNN layer have a larger receptive field with less computational cost.

### Fully Connected (FC)
Fully connected layer is comparable to Multilayer Perceptron which mimics the use of human brain. It connected with a mesh of connection between input and output nodes where the model learns to find a proper weight connection between input and output nodes.

### Optimization
Both CNN and FC learn it weights (and filters) using a gradient-based optimization method which is backpropagation algorithm. We can choose which optimizer to use from tensorflow's library.

### Architecture
We use 3 layers of convolution and max pool layers before flatten the feature maps to be a vector. After that, the vectorized feature map is passed to a fully connected layer with 128 units before passing to a classification layer (softmax layer) which emits output probabilities.

### Evaluation
According to the result, 96.25% seems to be an acceptable accuracy. However, there is still a lot of room to be improved for this model using the following techniques:

- Data Augmentation
- Batch Normalization
- Dropout
- etc.