# 2d_image_pre-processing

_2d medical image pre-processing for CNN model training_

**Intensity normalization**

Intensity normalization is good practice and should always be done prior to using data for training. Making all of your intensity values fall within a small range that is close to zero helps the weights on our convolutional filters stay under control

There are two types of normalization that you can perform.

* zero-meaning: subtract that mean intensity value from every pixel.
* standardization: subtract the mean from each pixel and divide by the image’s standard deviation.

**Image augmentation**

Image augmentation allows us to create different versions of the original data. Keras provides `ImageDataGenerator` package for image augmentation.

**Note**: not all image augmentation method is appropriate for medical imaging. A vertical flip should never be applied. And validation data should NEVER be augmented.

**Image resize**

CNNs have an input layer that specifies the size of the image they can process. Keras `flow_from_directory` have a `target_size` parameter to resize image.


