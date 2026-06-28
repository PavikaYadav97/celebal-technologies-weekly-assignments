# CIFAR-10 Image Classification using ANN and CNN

## Project Overview

This project focuses on building and comparing image classification models on the CIFAR-10 dataset using Artificial Neural Networks (ANN) and Convolutional Neural Networks (CNN).

The objective is to analyze how different deep learning architectures and training strategies affect image classification performance.

The project also explores various optimization techniques including:

- Increased ANN depth
- Enhanced CNN architectures
- Extended training epochs
- EarlyStopping
- Data Augmentation

---

## Dataset

The CIFAR-10 dataset contains 60,000 color images of size 32×32 pixels across 10 classes.

### Classes

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

### Dataset Split

- Training Images: 50,000
- Testing Images: 10,000

---

## Project Workflow

### 1. Data Loading
- Load CIFAR-10 dataset using TensorFlow/Keras

### 2. Data Visualization
- Display sample images from different classes

### 3. Data Preprocessing
- Normalize pixel values from 0–255 to 0–1
- Flatten images for ANN architecture

### 4. ANN Implementation
- Baseline ANN Model
- Deep ANN Architecture

### 5. CNN Implementation
- Standard CNN Model
- Enhanced CNN with additional filters

### 6. Training Strategy Experiments
- Increased Epochs
- EarlyStopping
- Data Augmentation

### 7. Model Evaluation
- Training Accuracy
- Validation Accuracy
- Test Accuracy
- Learning Curves

### 8. Performance Comparison
- ANN vs CNN
- Architecture Comparison
- Training Strategy Comparison

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib

---

## Training Strategies Evaluated

### Dropout
Used to reduce overfitting by randomly disabling neurons during training.

### Batch Normalization
Improves training stability and convergence speed.

### EarlyStopping
Stops training automatically when validation performance stops improving.

### Data Augmentation
Generates transformed versions of images through:
- Horizontal Flipping
- Rotation
- Zooming

This helps improve model generalization.

---

## Experimental Models

1. ANN (Baseline)
2. Deep ANN
3. CNN (Baseline)
4. Enhanced CNN
5. CNN with EarlyStopping
6. CNN with Data Augmentation

---

## Key Observations

- ANN achieved lower accuracy because image spatial information is lost after flattening.
- CNN significantly outperformed ANN by learning spatial features directly from images.
- Increasing ANN depth improved performance slightly but remained inferior to CNN.
- EarlyStopping helped prevent overfitting and improved generalization.
- Data Augmentation increased dataset diversity and improved model robustness.
- CNN-based architectures consistently delivered the best classification performance.

---

## Conclusion

This project demonstrates the effectiveness of Convolutional Neural Networks for image classification tasks.

While Artificial Neural Networks provide a useful baseline, CNNs achieve significantly higher performance by preserving spatial information and extracting hierarchical image features.

The experiments further show that training strategies such as EarlyStopping and Data Augmentation can improve model generalization and overall performance.

Overall, CNN-based architectures proved to be the most effective approach for CIFAR-10 image classification.

---

## Repository Structure

```text
├── CIFAR10_ANN_CNN_Submission_Ready.ipynb
├── README.md
├── requirements.txt
└── images/
```

---

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Install required libraries.
3. Run all cells sequentially.
4. Observe model training, evaluation metrics, and comparison results.

---

## Author

**Pavika Yadav**

B.Tech CSE (Data Science)  
Amity University  
Data Science Intern – Celebal Technologies
