# Using deep learning to classify fruits using the VGG16 model

## A. Data preprocessing
Collect data from kaggle [Dataset](https://www.kaggle.com/datasets/karimabdulnabi/fruit-classification10-class)
Create training, validation, and test data sets
Reshape the size
Mix photos
Normalize the data to [0,1] and the label converts to One-hot encoding

## B. Build model VGG16
Before you proceed to build the model, you should learn about the VGG16 structure.
![VGG-16-model-structure](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/591f9348-984f-4cf4-9142-2dec24801559)

[VGG16 structure](https://www.researchgate.net/figure/VGG-16-model-Illustration-of-using-the-VGG-16-for-transfer-learning-The-convolution_fig2_334992074)https://www.researchgate.net/figure/VGG-16-model-Illustration-of-using-the-VGG-16-for-transfer-learning-The-convolution_fig2_334992074)

The model I built includes:
4 layers Conv2D Layer: This is a convolutional layer, where each unit performs a convolution on the input to extract features. In this code, we use 2 Conv2D layers with 32 and 64 filters of size (3,3) and ReLU activation function.

4 layers BatchNormalization Layer: This layer performs normalization of the outputs of previous layers, helping to ensure that the values passed into the next layer are normalized. This improves learning speed and model stability.

2 layers MaxPool2D Layer: This layer performs local pooling on spatial regions of input data, reducing the size of the output and helping to reduce computational costs. In this code, we use MaxPool2D with pool_size=(2,2) and strides=(2,2).

Flatten Layer: This layer flattens data from a 2D matrix into a 1D vector, to prepare for connection with Fully Connected layers.

Dense Layer: This is a Fully Connected layer, in which each unit connects to all units in the previous layer. In this code, we use 2 Dense layers with 512 and 8 units, and the ReLU and softmax activation functions.

## C. Visualize model parameters
The loss of training and validation.

![屏幕截图 2024-03-21 234057](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/948f7fae-0de6-4ae5-a68d-7ef8c6679d7d)

The accuracy of training and validation.

![屏幕截图 2024-03-21 234109](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/1b87afbf-da75-4eeb-b8e3-cc387116431d)

Confusion matrix with data testing.

![屏幕截图 2024-03-21 234148](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/683b8f9c-0e7e-41c1-85f7-b43ad41bfc49)

Classification report.

![屏幕截图 2024-03-21 235413](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/8526fe73-1783-4d11-9ba4-11dfd0a1aad5)

## D. Save the model and reuse it

## E. Result
![屏幕截图 2024-03-21 235631](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/b908d21e-3dec-49fd-9d0b-13844c4c10a6)
![屏幕截图 2024-03-21 235607](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/f0a6ccfc-9576-4a2a-9168-10e8f3511df8)

### **Hope this article can help you.**
### **If you have any questions please contact me for help!**
### **Gmail: tuanddt.ai.work@gmail.com**

### ***Thanks everyone!***





