
# Coffee Disease Classifier

## Table of Contents
- [Coffee Disease Classifier](#coffee-disease-classifier)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Features](#features)
  - [Technologies Used](#technologies-used)
  - [Dataset](#dataset)
    - [Dataset Structure](#dataset-structure)
  - [Model Architecture](#model-architecture)
    - [Model Performance](#model-performance)
  - [Installation](#installation)
    - [Prerequisites](#prerequisites)
    - [Steps](#steps)
  - [Usage](#usage)
  - [Future Work](#future-work)
  - [License](#license)
  - [Contact](#contact)

## Overview
The **Coffee Disease Classifier** is a mobile application designed to identify and classify diseases in coffee plants using deep learning. The app leverages a Convolutional Neural Network (CNN) model, trained on a dataset of plant images, to detect and diagnose various coffee diseases from images taken by the user.

## Features
- **Disease Detection**: Identifies and classifies common coffee diseases.
- **Real-Time Analysis**: Users can take a photo or upload an image of a coffee plant for immediate analysis.
- **User-Friendly Interface**: Built with Flutter for a smooth and intuitive user experience.
- **Offline Capability**: The model can perform inference without an internet connection, making it suitable for use in the field.

## Technologies Used
- **TensorFlow**: For building and training the CNN model.
- **Keras (tf.keras)**: A high-level API for TensorFlow, used to simplify model development.
- **Flutter**: For creating the cross-platform mobile application.
- **Dart**: The programming language used with Flutter.

## Dataset
The model is trained and tested using the [Plant Disease Classification - Merged Dataset](https://www.kaggle.com/datasets/alinedobrovsky/plant-disease-classification-merged-dataset/data) available on Kaggle. The dataset contains images of various plant diseases, including those affecting coffee plants.

### Dataset Structure
- **Number of Classes**: 39 (includes various plant diseases and healthy plants). But in this project, we only use 4 classes: ```Coffee__cercospora_leaf_spot```, ```Coffee__healthy```, ```Coffee__red_spider_mite```, ```Coffee__rust```.
- **Number of Images**: Over 87,000 images. But we only use 1103 files belonging to the 4 classes.
- **Image Size**: 256x256 pixels

## Model Architecture
The CNN model was developed using the following architecture:
- **Input Layer**: Accepts 256x256x3 images.
- **Convolutional Layers**: Multiple layers with ReLU activation and max-pooling.
- **Fully Connected Layers**: Dense layers leading to the output classification.
- **Output Layer**: Softmax activation for multi-class classification.

### Model Performance
- **Accuracy**: Achieved an accuracy of approximately $75.98$ on the test set.
- **Loss**: Final loss value was $0.6019$ on the test set.

## Installation
### Prerequisites
- Flutter SDK
- Dart
- TensorFlow and Keras
- Python 3.x

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/TheMetaSetter/coffee-disease-classifier.git
   cd coffee-disease-classifier
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Install Flutter dependencies:
   ```bash
   flutter pub get
   ```

4. Run the application:
   ```bash
   flutter run
   ```

## Usage
1. Open the app on your mobile device.
2. Capture or upload an image of a coffee plant leaf.
3. The app will analyze the image and display the predicted disease and confidence score.

## Future Work
- **Model Optimization**: Improve the model's accuracy and reduce its size for faster inference on mobile devices.
- **Additional Disease Classes**: Expand the dataset to include more coffee-specific diseases.
- **Multi-Language Support**: Add support for multiple languages to increase accessibility.
- **Cloud Integration**: Enable cloud-based model updates and data collection for continuous learning.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
For any questions or suggestions, please contact:
- **Khoi Nguyen** - [nguyenanhkhoi0608@gmail.com](mailto:nguyenanhkhoi0608@gmail.com)
- GitHub: [TheMetaSetter](https://github.com/TheMetaSetter)
