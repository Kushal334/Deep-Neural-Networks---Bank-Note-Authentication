## Deep Neural Networks - Bank Note Authentication



In this project, I have implemented a 7 layer deep neural network for authentication of a dataset tht contains information about the various features of images of bank notes. This model classifes each observation into real or fake.


## About the data

1) This data has been taken from the UCI Machine Learning Repository
2) Data were extracted from images that were taken from genuine and forged banknote-like specimens. For digitization, an industrial camera usually used for print inspection was used
3) The final images have 400x 400 pixels. Due to the object lens and distance to the investigated object gray-scale pictures with a resolution of about 660 dpi were gained. Wavelet Transform tool were used to extract features from images
4) It consists of a total of 1373 instances


## Feature Description

1) Variance : variance of Wavelet Transformed image (continuous)
2) Skewness : skewness of Wavelet Transformed image (continuous)
3) Curtosis : curtosis of Wavelet Transformed image (continuous)
4) Entropy : entropy of image (continuous)
5) Class : class (integer - 0(Fake) or 1(Real))


## About the model

1) This model consists of 7 layers
2) It is purposely a complex model with high number of layers to combat the issue of high bias 
3) In order to initialize the weights in the appropriate manner, I have implemented He initialisation of weights to avoid the issue of exploding or vanishing gradients
4) This model consists of 6 layers that implement the Relu activation function and the output layer implements the sigmoid function


Please refer to *Notebook/BankNoteAuthentication.ipynb* for a detailed overview of the code I have written in Python for this implementation


## Results

I trained this model with a learning rate of 0.0075 and number of epochs = 8000( high number of epochs to combat the issue of high variance as we have less data to begin with)

Output:
1) Train accuracy : 0.9644484958979032
2) Test accuracy : 0.9636363636363636

Since, we have got a good accuracy of train as well as test data, we can conclude that our model has not overfit on the training data and it does not suffer from either high bias or high variance

Thank you!
