# Video-Classification-using-Keras-and-Tensorfloe
To count the number of defective and non defective bricks in a video file using tensorflow envoirnment
Approach Used: Convolutional Neural Network(CNN)
Dataset: Build up my own dataset using approx 5000 defective and non-defective bricks respectively to get good accuracy score.
Methodology Used: 
 	
  Data Exploration and Loading:(bricks.ipyb)
  
1) The defective and non-defective images were stored in different folders to categorize the images and indexed as 0: defective, 1: non-defective.
2) The data is read through importing os module from the required directory and images are read as grayscale images.
3) The training data is created by calling a function create_training_data() thus getting total training samples as 11139.
4) To extract and store the features and labels of the images the empty list x and y are created.
5) Using the pickle module data is serialized and de-serialized for creation of model.
 	
  Model Building:(model building_bricks.ipyb)

1) Model is build on tensorflow environment using keras by importing CNN2D and various other important layers which I have used in building model.
2) The 3 layers on Conv2D are used each using filter size of 32 with 3 MaxPooling layers.
The dropout of 0.25 is used followed by flattening and two dense layers of size 64 and 1 respectively. The relu activation function is used with earlier Dense layer and latter layer is passed through softmax activation function.
3) The model is fitted with 10 epochs with validation split of 0.1 and model summary is printed.
The obtained accuracy for model is 51.62 % and CNN error of 48.46%.
4) Model is saved as h5 file.
