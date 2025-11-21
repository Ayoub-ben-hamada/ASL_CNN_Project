# ASL CNN Project

This project implements a **Convolutional Neural Network (CNN)** to classify **American Sign Language (ASL)** images using **PyTorch**.

## Dataset

The dataset consists of grayscale ASL images in CSV format:
- `sign_mnist_train.csv` → training set
- `sign_mnist_valid.csv` → validation set

Images are flattened and need to be reshaped into **28x28 pixels** for CNN input.

## Project Steps

1. **Data Preparation**  
   - Reshape images to 28x28x1 (height x width x channels)
   - Normalize pixel values to range [0,1]

2. **Dataset & DataLoader**  
   - Custom `MyDataset` class for PyTorch
   - `DataLoader` for batching training and validation data

3. **CNN Architecture**  
   - 3 convolutional layers (`Conv2d`) with `BatchNorm2d`, `MaxPool2d` and `Dropout`
   - Flatten layer and fully connected layers (`Linear`) for classification
   - Output layer: 24 classes (A-Y without J)

4. **Training**  
   - Loss function: `CrossEntropyLoss`
   - Optimizer: `Adam`
   - Tracks training and validation accuracy per epoch

5. **Results**  
   - The CNN improves accuracy significantly over a simple dense network
   - Validation accuracy still fluctuates, showing possible improvements with data augmentation

## How to run

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/ASL_CNN_Project.git
