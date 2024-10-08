# ImageClassificationUsingCNN
This repository contains deep learning projects that utilize convolutional neural networks (CNNs) to classify images. The focus is on image classification, particularly using the CIFAR-10 dataset. This is for UCSD's SPIS 2024 final project, but also is a personal project.

## Features
- **Deep Learning Model**: Implements a convolutional neural network for image classification.
- **PyTorch Implementation**: Efficient and flexible model training and evaluation using PyTorch.

## Project Structure

```
ImageClassifierModel/
│
├── data/                   # Folder containing datasets
│
├── Saved_Models/           # Folder containing all Model experimentation
│
├── Web_Application/        # Folder containing web application for model
│   ├── static/             # Folder containing css and uploads folder
│   ├── templates/          # Folder containing templates in html
│   └── app.py              # Runs web application via Flask
│
├── demo.py                 # File containing demo of preselected model
│
├── main_cirfar10.py        # File containing training/saving of model for CIFAR-10 
│
├── main_cifar100.py        # File containing training/saving of model for CIFAR-100 (Not working)
│
└── model.py                # File containing model architecture via Pytorch
```

### ImageClassifierModel (More in depth info)
This folder focuses on classifying images from the CIFAR-10 dataset using a convolutional neural network. The model assigns images to one of 10 classes. The folder contains the following key components:

- `data/`: Contains the CIFAR-10 and CIFAR-100 datasets.

- `Saved_Models/`: Stores the trained models.

- `main_cifar10.py` & `main_cifar100.py`: These scripts handle dataset loading, model training, and saving the trained model locally. `main_cifar10.py` is used for CIFAR-10, while `main_cifar100.py` will be used for CIFAR-100.

- `model.py`: Defines the convolutional neural network architecture used for classification.

- `demo.py`: Demonstrates the model by randomly selecting images from the CIFAR-10 or CIFAR-100 dataset and classifying them using the trained model.

#### Saved Model Naming Convention:
- **First four digits**: Accuracy
- **Fifth digit**: Experiment Number
- **Rest of the name**: Model Name (e.g., cifar10_cnn)
## Installation
To install the required dependencies, use the following command:

```
pip install numpy torch torchvision pillow matplotlib tqdm flask
```

- **NumPy**: For numerical operations and array manipulation.
- **PyTorch**: The core deep learning library for building and training the model.
- **TorchVision**: Utilities for image processing and loading datasets.
- **Pillow**: For opening and processing images and image manipulation.
- **Matplotlib**: For visualizing results.
- **TQDM**: For progress visualization.
- **Flask**: For website demos.

> Python Version: 3.10

## How to Run the Model
1. **Prepare Data**: Ensure that your dataset is ready in the `data/` folder.

2. **Train the Model**: Run the `main_cifar10.py` script to download the dataset, train the model, and save the trained model.

3. **Demo the Model**: Run the `demo.py` script to demo the model. The demo randomly selects images from the CIFAR-10 or CIFAR-100 dataset and classifies them using the locally saved model.
