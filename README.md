# Using deep learning to classify fruits using the VGG16 model
## A. Data preprocessing
*Create training, validation, and test data sets
*Reshape the size
*Mix photos
*Normalize the data to [0,1] and the label converts to One-hot encoding
## B. Build model VGG16
Before you proceed to build the model, you should learn about the VGG16 structure.
![VGG-16-model-structure](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/591f9348-984f-4cf4-9142-2dec24801559)
[VGG16 structure]([https://thigiacmaytinh.com](https://www.researchgate.net/figure/VGG-16-model-Illustration-of-using-the-VGG-16-for-transfer-learning-The-convolution_fig2_334992074)https://www.researchgate.net/figure/VGG-16-model-Illustration-of-using-the-VGG-16-for-transfer-learning-The-convolution_fig2_334992074)
The model I built includes:
4 layers Conv2D Layer: This is a convolutional layer, where each unit performs a convolution on the input to extract features. In this code, we use 2 Conv2D layers with 32 and 64 filters of size (3,3) and ReLU activation function.

4 layers BatchNormalization Layer: This layer performs normalization of the outputs of previous layers, helping to ensure that the values passed into the next layer are normalized. This improves learning speed and model stability.

2 layers MaxPool2D Layer: This layer performs local pooling on spatial regions of input data, reducing the size of the output and helping to reduce computational costs. In this code, we use MaxPool2D with pool_size=(2,2) and strides=(2,2).

Flatten Layer: This layer flattens data from a 2D matrix into a 1D vector, to prepare for connection with Fully Connected layers.

Dense Layer: This is a Fully Connected layer, in which each unit connects to all units in the previous layer. In this code, we use 2 Dense layers with 512 and 8 units, and the ReLU and softmax activation functions.

## C. Visualize model parameters
* The loss of training and validation
![屏幕截图 2024-03-21 234057](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/948f7fae-0de6-4ae5-a68d-7ef8c6679d7d)
* The accuracy of training and validation
![屏幕截图 2024-03-21 234109](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/1b87afbf-da75-4eeb-b8e3-cc387116431d)
* Confusion matrix with data testing
![屏幕截图 2024-03-21 234148](https://github.com/FPT-ThaiTuan/Using-deep-learning-to-classify-fruits-using-the-VGG16-model/assets/105273233/683b8f9c-0e7e-41c1-85f7-b43ad41bfc49)
* Classification report
|  | precision | recall | f1-score | support |
| :—–--- | :———- | :————– | :———- | :————– |
| banana | 0.75  | 0.75  | 0.75  | 4 |
| avocado | 1.00 | 0.80 | 0.89 | 5 |
| 2 | Dòng 12 | Dòng 22 |Dòng 11 | Dòng 21 |  cherry       0.83      1.00      0.91         5
| 3 | Dòng 13 | Dòng 23 |Dòng 11 | Dòng 21 |  kiwi       1.00      1.00      1.00         5
| 4 | Dòng 14 | Dòng 24 |Dòng 11 | Dòng 21 | mango       0.75      0.60      0.67         5
| 3 | Dòng 13 | Dòng 23 |Dòng 11 | Dòng 21 | orange       1.00      1.00      1.00         4
| 3 | Dòng 13 | Dòng 23 |Dòng 11 | Dòng 21 | pinenapple       0.67      0.80      0.73         5
| 4 | Dòng 14 | Dòng 24 |Dòng 11 | Dòng 21 | watermelon       1.00      1.00      1.00         5
| 2 | Dòng 12 | Dòng 22 |Dòng 11 | Dòng 21 |   accuracy                           0.87        38
| 2 | Dòng 12 | Dòng 22 |Dòng 11 | Dòng 21 | macro avg       0.88      0.87      0.87        38
| 2 | Dòng 12 | Dòng 22 |Dòng 11 | Dòng 21 |weighted avg       0.88      0.87      0.87        38
| 3 | Dòng 13 | Dòng 23 |
| 4 | Dòng 14 | Dòng 24 |
