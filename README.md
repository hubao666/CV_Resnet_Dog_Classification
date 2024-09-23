# Dog Classification Using ResNet Transfer Learning
## To run the code:
- Download the dataset from Stanford Dogs Dataset
- Extract both Images and Annotations .tar files
- Place the extracted contents into directories (Images and Annotations)
- Use the provided notebook to train and evaluate the model
## Topic
This project applies transfer learning using a pre-trained ResNet-18 model to classify dog breeds. The last fully connected layer is modified to adapt to the number of target classes.

## Method
### Data Preparation:
- Images are resized to 224x224, converted to tensors, and normalized. The dataset includes original images, cropped images based on bounding box annotations, and augmented cropped images.
- Three types of data are used: original images, cropped images, and augmented cropped images.
### Model Variations:
- ResNet-18 pre-trained on ImageNet, with variations including:
    - A single modified fully connected layer
    - Two additional fully connected layers with ReLU and dropout
### Training Setup:
Four combinations of model and dataset type were trained and evaluated:
  - 1 fully connected layer & original images
  - 2 fully connected layers & original images
  - 1 fully connected layer & cropped images
  - 2 fully connected layers & augmented cropped images
The model is trained for 10 epochs using cross-entropy loss, the SGD optimizer, and learning rate scheduling.
## Result
- The model with 1 modified fully connected layer trained on cropped images performed best:
- Train Accuracy: 99.99%
- Test Accuracy: 79.71%
