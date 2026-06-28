# Week 6: Image Denoising using Autoencoder on MNIST

## Project Overview

This project demonstrates the use of a Convolutional Autoencoder for image denoising on the MNIST handwritten digit dataset. The objective is to train a deep learning model capable of reconstructing clean images from noisy inputs by learning compressed feature representations.

The autoencoder consists of an Encoder that extracts meaningful features from noisy images and a Decoder that reconstructs denoised images from the compressed representation.

---

## Objectives

* Load and preprocess the MNIST dataset.
* Generate artificially corrupted images using Gaussian noise.
* Build and train a Convolutional Autoencoder.
* Reconstruct clean images from noisy inputs.
* Evaluate denoising performance using:

  * Training and Validation Loss
  * Mean Squared Error (MSE)
  * Visual comparison of original, noisy, and reconstructed images
* Analyze model performance and reconstruction quality.

---

## Dataset

**MNIST Handwritten Digits Dataset**

* 60,000 training images
* 10,000 testing images
* Grayscale images of size 28×28 pixels
* Digit classes: 0–9

The dataset is loaded directly using TensorFlow/Keras.

---

## Methodology

### 1. Data Preprocessing

* Normalize pixel values to the range [0,1].
* Reshape images to include channel dimensions.

### 2. Noise Generation

* Add Gaussian noise to create corrupted input images.
* Clip pixel values to maintain valid image ranges.

### 3. Autoencoder Architecture

#### Encoder

* Conv2D (32 filters)
* MaxPooling2D
* Conv2D (64 filters)
* MaxPooling2D

#### Decoder

* Conv2D (64 filters)
* UpSampling2D
* Conv2D (32 filters)
* UpSampling2D
* Output Conv2D Layer

### 4. Model Training

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Epochs: 10
* Batch Size: 128

---

## Results

### Training Performance

Training and validation losses decreased consistently throughout training, indicating successful learning and stable convergence.

### Quantitative Evaluation

**Reconstruction MSE: 0.0110**

A low Mean Squared Error value indicates that the reconstructed images are highly similar to the original clean images.

### Visual Evaluation

The model successfully:

* Removed a significant amount of Gaussian noise.
* Preserved the overall structure of handwritten digits.
* Reconstructed recognizable digit images from heavily corrupted inputs.

---

## Key Observations

* The autoencoder effectively learned compressed representations of digit images.
* Significant noise reduction was achieved while retaining important visual features.
* Some reconstructed images appear slightly blurred due to information compression during encoding.
* Training and validation losses remained close throughout training, indicating minimal overfitting.

---

## Limitations

* Evaluation relies primarily on reconstruction loss, MSE, and visual inspection.
* Only Gaussian noise was considered during training.
* The model was tested on the relatively simple MNIST dataset.
* More complex real-world image denoising tasks may require deeper architectures and additional evaluation metrics.

---

## Conclusion

A Convolutional Autoencoder was successfully implemented for image denoising on the MNIST dataset. The model learned to reconstruct clean handwritten digit images from noisy inputs with low reconstruction error and stable training performance.

The results demonstrate the effectiveness of autoencoders for image restoration tasks and provide a strong foundation for exploring advanced deep learning applications in computer vision.

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Scikit-learn

---

## Assignment Details

**Week 6 Assessment – Deep Learning**

**Project Title:** Image Denoising using Autoencoder on MNIST Dataset

**Objective:** Build a deep learning model capable of removing noise from images using an Autoencoder and evaluate its denoising performance through reconstruction quality and quantitative metrics.
