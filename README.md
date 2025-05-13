# Arrow Detection Using ResNet18

This project evaluates the effectiveness of the ResNet18 model for arrow detection as part of our university rover project. The goal is to identify directional arrows (e.g., "left", "right") from images captured in a campus or lab environment.

## Overview

- **Framework:** PyTorch with TorchVision  
- **Model:** Pre-trained ResNet18 fine-tuned on a custom arrow dataset  
- **Data:**  
  - Training and validation images are located in the `dataset/train` and `dataset/val` folders respectively.
  - Additional test images for inference are located in the `test` folder.
- **Notebook:** The entire training, evaluation, and inference pipeline is implemented in [image_classification.ipynb](e:\MyDocuments\All Codes\Arrow Detection Model Validation\Arrow-Detection-Model-Validation\image_classification.ipynb).

## Features

- **Data Augmentation and Normalization:**  
  Utilizes different transformations for training (random resized crop) and validation (resize).

- **Model Training:**  
  The notebook freezes all layers except the final fully-connected layer of ResNet18. The training loop shows loss and accuracy per epoch on both training and validation sets.

- **Model Saving & Inference:**  
  Once training is complete, the model is saved as `arrow_classification_model_Version_X.pth`. 
  
- **Visualization:**  
  I Used Matplotlib to display the test images along with the predicted class labels.

## Setup & Usage

1. **Install Dependencies:**  
   Ensure you have Python, PyTorch, and TorchVision installed. You may also need PIL and Matplotlib:
   ```sh
   pip install torch torchvision pillow matplotlib
