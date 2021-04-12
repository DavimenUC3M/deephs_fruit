# Measuring the Ripeness of Fruit with Hyperspectral Imaging and Deep Learning

<em>(This is the version for the review process of the IJCNN 2021. The final version is planned on GitHub)</em>

Here you can find the data set and the implementation of the HS-CNN network.

## Dataset
The dataset is here available. It contains 1038 hyperspectral recordings of avocados and 1522 hyperspectral recordings of kiwis. The ripening process from unripe to overripe is covered. Because of the destructive manner of the labeling process, only 180 avocado recordings and 262 kiwis recordings are labeled by indicator measurements.
Two cameras (Specim FX 10 and INNO-SPEC Redeye 1.7) were in two measurement  series covering a total of 28 days in the years 2019 and 2020.

## HS-CNN
This is the official implementation of the HS-CNN network. This implementation is based on PyTorch and PyTorch Lightning.

The code is divided into subfolders, which correspond to the use cases:
 - 'classification' contains the training process for the classification task. Here you can find the implementation of HS-CNN, AlexNet, ResNet-18, SVM and kNN.
 - 'extract_fruit' trains a layer classifier and extracts the fruits.
 - 'false_color_images' defines the two stage training process of the autoencoder and the classification network. This allows the visualization of the ripening process.
 - 'core' contains the basic components. (IO, loss functions)