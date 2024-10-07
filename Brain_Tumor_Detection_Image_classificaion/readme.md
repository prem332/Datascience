# Brain Tumor Detection Image Classification

## Project Overview
This project aims to develop a reliable and efficient image classification system for detecting brain tumors using deep learning techniques. The system utilizes Convolutional Neural Networks (CNN) to classify medical images into four distinct categories of brain tumors: **pituitary**, **notumor**, **meningioma**, and **glioma**.

## Total Number of Classes
- **Total Classes:** 4
- **Class Names:** 
  - Pituitary
  - Notumor
  - Meningioma
  - Glioma

## Methodology
### Data Collection
Images were collected from various medical databases and public repositories to create a diverse dataset. The dataset was divided into training, validation, and testing sets.

### Model Selection
Three deep learning models were experimented with:
1. **VGG16**
   - **Accuracy Achieved:** 96%
2. **ResNet**
   - **Accuracy Achieved:** 92%
3. **Traditional CNN**
   - **Accuracy Achieved:** 89%

### Data Preprocessing
- Resized images to standard dimensions.
- Normalized pixel values.
- Applied data augmentation techniques to enhance dataset diversity.
