# Dog vs. Cat Image Classifier

**Project Description**  
This repository contains a convolutional neural network (CNN) image classifier that distinguishes between **dogs** and **cats**.  
The project was developed following the YouTube tutorial **“Dog vs. Cat Image Classification in Python”**  
https://www.youtube.com/watch?v=ENXr1foShrA  

The model is trained using TensorFlow/Keras, with image preprocessing and data augmentation to improve generalization.  

---

## Table of Contents
- [Dataset](#dataset)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Model Architecture](#model-architecture)  
- [Training](#training)  
- [Results](#results)

---

## Dataset  
We use the **Microsoft Cats vs. Dogs dataset**, originally published on Kaggle and later hosted by Microsoft.  
- Link: https://www.microsoft.com/en-us/download/details.aspx?id=54765  
- The dataset consists of **25,000 images** equally divided into **cats** and **dogs**.  

For training and validation:  
- Images are resized to **128x128 pixels**.  
- The dataset is split into **training** and **validation** subsets.

---

## Installation  

1. **Clone the repository**
   ```bash
   git clone https://github.com/xKazimir/DOG-CAT-IMAGE-CLASSIFIER.git
   cd DOG-CAT-IMAGE-CLASSIFIER
2. **Create & activate a virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # on Linux/Mac
   venv\Scripts\activate      # on Windows
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   
## Usage
Open the Jupyter notebook:
   ```bash
   jupyter notebook
   ```
Run the notebook catdog image classifier.ipynb step by step:
- Data loading & preprocessing
- Data augmentation (rotation, shear, zoom, flips)
- Model building & training
- Evaluation & prediction

To make a prediction on a custom image insert the path to the image into this line in the last cell:
   ```python
   image_path = "insert path to image"
   ```

## Model Architecture
The CNN architecture is built using Keras Sequential API:
 - Convolutional layers with ReLU activation
 - MaxPooling layers for downsampling
 - Flatten layer to convert feature maps into vectors
 - Dense (fully connected) layers with dropout for regularization
 - Sigmoid output layer for binary classification
## Training
 - ImageDataGenerator is used for real-time data augmentation:
   - Normalization (rescale=1./255)
   - Rotation, shear, zoom, and horizontal flips
 - Optimizer: Adam
 - Loss function: Binary Crossentropy
 - Metric: Accuracy
 - Model trained for multiple epochs until convergence.

## Results
 - The model achieves high accuracy (~85–90%) on validation data.
 - Sample predictions correctly classify cats and dogs.

## Credits  

- Tutorial: [Dog vs. Cat Image Classification in Python](https://www.youtube.com/watch?v=ENXr1foShrA)  
- Dataset: [Microsoft Cats vs. Dogs](https://www.microsoft.com/en-us/download/details.aspx?id=54765)  
