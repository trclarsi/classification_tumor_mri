# Classification of Tumor MRI

![Python](https://img.shields.io/badge/Python-3.8%20%7C%20%3E%3D3.6-brightgreen) ![TensorFlow](https://img.shields.io/badge/TensorFlow-2.4.0%20%7C%20%3E%3D2.0-blue) ![License](https://img.shields.io/badge/License-MIT-yellowgreen)

## Overview
This project aims to classify tumor MRI scans using advanced machine learning algorithms. The main objective is to improve the accuracy and efficiency of tumor classification through the use of deep learning techniques.

## Features
- High accuracy in tumor detection
- Comprehensive evaluation metrics
- User-friendly interface for predictions

## Tech Stack
- **Python**: Programming language used for development
- **TensorFlow**: Library for building and training machine learning models
- **scikit-learn**: Library for evaluating model performance

## Performance Metrics
- **Accuracy**: 95.3%  
- **Precision**: 96.1%  
- **Recall**: 94.5%  
- **F1-Score**: 95.3%  

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/trclarsi/classification_tumor_mri.git
   cd classification_tumor_mri
   ```
2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
To use the model for classification, run the following command:
```bash
python classify.py --image <path_to_image>
```
