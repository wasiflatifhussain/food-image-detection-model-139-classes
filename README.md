# food-image-detection-model-139-classes
Training a convolutional neural network (CNN) model for image classification using transfer learning with the DenseNet-201 architecture

### Datasets used:
This project combines classes from the Food-101 dataset and the Food-2k dataset, as well as other images from online resources to increase the dataset for each classes. The Food-2k dataset contained multiple duplicate images and classes and incorrect classifications. Hence, as part of this project, I worked on collecting unique data classes from the Food-2k dataset, combining common/similar classes to make superclasses that could be used to identify a category of food. The work involved cleaning data, summarizing dataset classes, as well as adding more images for smaller classes to increase the volume of data for each data classes and to bring consistency to the dataset size for each data classes.


### Training and Architecture:
This code is for training a convolutional neural network (CNN) model for image classification using transfer learning with the DenseNet-201 architecture. The DenseNet-201 model is pre-trained on the ImageNet dataset, and the final fully connected layer is replaced with a new one for 139 classes of food items.

Model Definition: 
The DenseNet-201 model is loaded from torchvision.models and modified by replacing the final classifier with a new one suitable for 139 classes.

Evaluation:
Upon training completion, the model undergoes evaluation using the test dataset. The evaluation process employs the evaluate function, which computes the accuracy of the model's predictions. This metric serves as a critical indicator of the model's performance in accurately classifying food images across the 139 distinct classes.

### Installation

To install the required dependencies, you can use `pip`. First, clone the repository:

```bash
git clone https://github.com/your_username/food-139-classification.git
cd food-139-classification
