## Part1  

print(score): [0.04471985881958621, 0.9905]


## Part2

**1. Convolution:**
Convolution is the process of adding each element of the image to its neighbors, weighted by the kernel.

**2. Filters/Kernels:** 
In Image processing to extract features we use small matrices (3x3,5x5 e.t.c.). This matrix helps us extract mutiple feature channels like edge detectors, horizontal detectors etc. A kernel can also be viewed as a `filter or feauture extractor` that can help us in manipulating and extracting parts of image for further analysis. Some of the examples can be blur kernel, sharpen kernel which are manually created kernels. Below you can see a vertical edge detector.
  
  ![Image](https://drive.google.com/uc?id=10jbReSFLy4Sm_2CKWRzKVvq1bhQRRwvw) 
    
**3. Epochs:** 
While training the Network, One Epoch is a iteration of Cost function optimization(training) over full training image set once.

**4. 1x1 Convolution:** 
General architecture of a cnn is to increase the number of channels so that we can understand more feautres of the input and then decrease the number of channels to combine these learning and equate them to our prediction channels. 1x1 convolution is an effective way to decrease the number of channels or feature maps. It works very effectively as a aggregator of predominant features when back propagation is used to train the model.It basically multiplies the every channel of that layer with a value(kernel weight) and add them.

**5. 3x3 Convolution:**
It is most commonly used kernel size for image convolution. Generally odd nummbered kernel size is used for image convolution as symmetry is maintained while extracting the information from certain pixel and passed to next layer. As we loose information as part of convolution, 3x3 is the best option as its the first odd numbered matrix after 1X1. 

**6. Feature Maps:**
A kernal convolutes over an image to extract features. This output of extracted feature is called feature map or Channel. A group/layer of similar characteristics of an image can be considered as a channel. Below figure you can observe that same peacock is divide into 3 layers of characterics that is a pixel value for colour green, red and blue. An image can be broken into any number of channels.
 
  ![Image](https://drive.google.com/uc?id=1quPLiZewo9yxQEsJohcOkwC_mmehAp0j)
  
**7. Activation Function:** 
Any function that can be used at every neuron to induce non linearity in the network is know as an Activation Function. Eg: Relu, Selu, Sigmoid, Tanh e.t.c
    
**8. Receptive Field:** 
Number of pixels from the input image that a particular kernel would use to extract information at a particular layer is called local receptive field. For example a 1st layer 3x3 kernel would have a receptive field of 3x3. Similarly, a 2nd layer 3x3 kernel would have a recptive field would be 5x5. Number of pixels from the input image that the last prediction layer kernel would use to extract the information is called global receptive field.
