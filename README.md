# Brain-Tumor-Detection
Building a detection model using a Convolutional neural network in Tensorflow &amp; Keras. Used a brain MRI images dataset
Building a detection model using a convolutional neural network in Tensorflow & Keras.
Used a brain MRI images data founded on Kaggle. You can find it here.

About the data:
The dataset contains 2 folders: yes and no which contains 253 Brain MRI Images. The folder yes contains 155 Brain MRI Images that are tumorous and the folder no contains 98 Brain MRI Images that are non-tumorous.


# Data Augmentation:
Since this is a small dataset, There wasn't enough examples to train the neural network. Also, data augmentation was useful in taclking the data imbalance issue in the data.

Further explanations are found in the Data Augmentation notebook.

Before data augmentation, the dataset consisted of:
155 positive and 98 negative examples, resulting in 253 example images.

After data augmentation, now the dataset consists of:
1085 positive and 980 examples, resulting in 2065 example images.


# Data Preprocessing
For every image, the following preprocessing steps were applied:

1-)Crop the part of the image that contains only the brain (which is the most important part of the image).
2-)Resize the image to have a shape of (240, 240, 3)=(image_width, image_height, number of channels): because images in the dataset come in different sizes. So, all images should have the same shape to feed it as an input to the neural network.
3-)Apply normalization: to scale pixel values to the range 0-1.

# Data Split:
The data was split in the following way:

1-)70% of the data for training.
2-)15% of the data for validation.
3-)15% of the data for testing.

# Neural Network Architecture
This is the architecture that I've built:


![convnet_architecture](https://user-images.githubusercontent.com/19469956/68879258-f065a400-06bd-11ea-8c4e-499a13d59ca2.jpg)



