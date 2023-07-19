# Image-Classification-using-CNN
 Convolutional Neural Network model is build for Image Classification

 Here, images of fruits and other images are choosen randomely and formed dataset. The dataset contains 497 images of 6 Classes - ApplePie , Bibimbop,Bread, FriedRice,BagelSandwich and Pork. 

### Dependence
```
tensorflow
keras
numpy
pandas
PIL
```
### To Execute the Code :
1. Give the dataset path ('data_dir') and split train('train_dir') and test('test_dir') directory.
2. To display single image, load the image with filename.
3. Once model is created and accuracy is producted for test dataset, to validate single image- load the image and model.predict will predict the class of the given image. 
### Training and Testing Dataset
Here, training set with 497 images and testing set with 150 images are taken.
### Creating the Model
To create this model, here used Keras's sequential model. First, ‘empty’ sequential model is called. Then, the first layer is a convolutional layer with a depth of 32 and a filter size of 3x3. The activation is ‘relu’ (remain the same for all layers except the last one).

We need to specify an input size only for our first layer as the subsequent layers can infer the input size from the output size of the previous layer. Here, our input size is (224,224, 3).

There is a MaxPooling2D layer after every convolutional layer. This layer downsamples the input representation by taking the maximum value over a window. ‘Pooling’ is basically the process of merging for the purpose of reducing the size of the data.

Lastly, added Flatten and a Dropout (with a probability of 0.4) layer to the model. Flatten converts the data into a 1-dimensional array for inputting it to the next layer. Dropout is a way to prevent overfitting in neural networks.

Printed model summary to see how the model looks like overall.

### Specify the number of epochs and batch_size for the model
### Image Generator
For the purpose of augmentation, like Random shifting, rotation, zooming, and rescaling are some of the operations which can be done by ImageDataGenerator.
### Model Fit with Training Set
### Ploting the Loss and Accuracy
### Prediction is done for Testing Directory and Single Image 

#### Here, this model is done using CNN on Google Colab. 
## For 50 Epochs, loss: 0.3125 - accuracy: 0.9271 - val_loss: 0.1992 - val_accuracy: 0.9600. Here,testing accuracy is 96% , this can be improved further upon increasing epochs and fine tuning. 







 
 
