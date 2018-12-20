# German-Traffic-Signs-Classification
Solving German Traffic Signs Classification problem with VGG model 
Framework: Keras with Tensorflow - backend
Notebook: Googlecolab

## Introduction
-------------------------------------------
The German Traffic Sign Benchmark is a multi-class, single-image classification challenge held at the International Joint Conference on Neural Networks (IJCNN) 2011. The dataset contains more than 30K photos with 43 different classes. 

#### Preprocessing
-------------------------------------------
To make it easier for the model to classify between the different signs I tried few classical image processing methods such as: thresholding, histogram equalization etc'.
The best results acheived with adaptive histogram equalization. This method usually increases the global contrast of many images, especially when the usable data of the image is represented by close contrast values. Through this adjustment, the intensities can be better distributed on the histogram. This allows for areas of lower local contrast to gain a higher contrast. Histogram equalization accomplishes this by effectively spreading out the most frequent intensity values.

#### Model 
-------------------------------------------
The proposed model is a variation of the classical VGG model.
VGGNet is a neural network that performed very well in the Image Net Large Scale Visual Recognition Challenge (ILSVRC) in 2014. It scored first place on the image localization task and second place on the image classification task.

![alt-text](https://www.abtosoftware.com/assets/17.png)

#### Training
-------------------------------------------
In the preprocessing stage I plotted the histogram of the classes, its easy to see that the histogram is not uniformed. In order to deal with this problem I used the `class_weight` option inside `model.fit` as documented at Keras.

#### Results
-------------------------------------------
The model achieved ~96% accuracy, the results are shown in confustion matrix and also been printed for each class

### Note
You don't need to download or to install anything to run this notebook! Just run the cells - the data is dowloaded automatically. 
