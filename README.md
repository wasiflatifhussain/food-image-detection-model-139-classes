# food-image-detection-model-139-classes
Training a convolutional neural network (CNN) model for image classification using transfer learning with the DenseNet-201 architecture

### Datasets used:
This project combines classes from the Food-101 dataset and the Food-2k dataset, as well as other images from online resources to increase the dataset for each classes. The Food-2k dataset contained multiple duplicate images and classes and incorrect classifications. Hence, as part of this project, I worked on collecting unique data classes from the Food-2k dataset, combining common/similar classes to make superclasses that could be used to identify a category of food. The work involved cleaning data, summarizing dataset classes, as well as adding more images for smaller classes to increase the volume of data for each data classes and to bring consistency to the dataset size for each data classes.

The dataset can be downloaded from the google drive link here: https://drive.google.com/file/d/1cP0ba1wjhiid-IjJQ29EsTFFteBQoylw/view?usp=sharing

Download and extract the zip folder and place it in the same directory as the rest of the code files.
#### To extract the zip file:

For Windows:
```
tar -xf food-101-tester.zip
```

For Mac:
```
unzip food-101-tester.zip
```

### Training and Architecture:
This code is for training a convolutional neural network (CNN) model for image classification using transfer learning with the DenseNet-201 architecture. The DenseNet-201 model is pre-trained on the ImageNet dataset, and the final fully connected layer is replaced with a new one for 139 classes of food items.

Model Definition: 
The DenseNet-201 model is loaded from torchvision.models and modified by replacing the final classifier with a new one suitable for 139 classes.

Evaluation:
Upon training completion, the model undergoes evaluation using the test dataset. The evaluation process employs the evaluate function, which computes the accuracy of the model's predictions. This metric serves as a critical indicator of the model's performance in accurately classifying food images across the 139 distinct classes.

### Installation

To install the required dependencies, you can use `pip`. First, clone the repository:

```bash
git clone https://github.com/wasiflatifhussain/food-image-detection-model-139-classes.git
cd food-image-detection-model-139-classes
```

To install the dependencies:

```bash
pip install -r requirements.txt
```

### Training Technique
Adjust the following parameters to train:
- Learning Rate, lr
- Batch Size, batch_size
- Number of iterations/epochs, num_epochs
- File Name, save_file_name

After adjusting the following parameters in the train.py file, run the following command:
```
python train.py
```

### Inference Technique
Run an inference an image to check model performance:
```
python inference.py <image_path> <state_dictionary_pth_file>
```

Example of an inference:
```
python inference.py ./zgz.jpeg ./saved_model_dictionary_139_class.pth
```
