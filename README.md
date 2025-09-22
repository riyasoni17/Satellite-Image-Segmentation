# Satellite Image Segmentation  

This repository contains my **Final Year Project (2023)** on **Satellite Image Segmentation** using deep learning techniques. The project focuses on **semantic segmentation of aerial imagery** to classify pixels into different land cover categories.  

---

## Problem Statement  
Given satellite images, the task is to assign each pixel to one of the following semantic classes:  

1. **Building** – `#3C1098`  
2. **Land (unpaved area)** – `#8429F6`  
3. **Road** – `#6EC1E4`  
4. **Vegetation** – `#FEDD3A`  
5. **Water** – `#E2A929`  
6. **Unlabeled** – `#9B9B9B`  

---

## Dataset  
- **Source:** [Kaggle – Semantic Segmentation of Aerial Imagery](https://www.kaggle.com/humansintheloop/semantic-segmentation-of-aerial-imagery)  
- **Description:** 72 satellite images of Dubai, grouped into 6 tiles, with corresponding pixel-level annotations.  
- **Format:** RGB images + masks with HEX-coded labels.  
- **Preprocessing:** Images were divided into **256×256 patches** for training.  

---

## Methodology  
1. **Data Preprocessing**  
   - Patch extraction (256×256)  
   - HEX to RGB conversion  
   - RGB to integer label mapping  
   - Normalization and scaling  

2. **Image Augmentation**  
   - Rotation, flipping, scaling, and brightness adjustments  

3. **Model Architecture**  
   - Implemented **U-Net based convolutional neural network** for semantic segmentation  
   - Encoder-decoder structure with skip connections  

4. **Training**  
   - Optimizer: Adam  
   - Loss function: Categorical cross-entropy  
   - Evaluation metric: Accuracy & IoU (Intersection over Union)  

5. **Results & Visualization**  
   - Segmented outputs compared against ground-truth masks  
   - Visual inspection confirms accurate separation of land, water, vegetation, and built-up areas  

---

## Results  
- Successfully segmented satellite images into six classes  
- Achieved high accuracy on validation data  
- Clear distinction observed in masks for **urban vs. natural features**  

---

## How to Run  
1. Clone the repository:  
   ```bash
   git clone https://github.com/riyasoni17/Satellite-Image-Segmentation.git
   cd Satellite-Image-Segmentation
   ```

2. Open the Jupyter Notebook:  
   ```bash
   jupyter notebook SATELLITE_IMAGE_SEGMENTATION_CODE.ipynb
   ```

3. Run all cells step by step to:  
   - Preprocess data  
   - Train the model  
   - Visualize segmentation results  

---

## Future Work  
- Train on larger datasets for improved generalization  
- Compare U-Net with **SegNet, DeepLabV3+**  
- Deploy as a **web-based GIS tool** for real-time segmentation  

---

## Author  
**Riya Soni**  
  LinkedIn: https://www.linkedin.com/in/riya-soni-oct01/
  Email: riyasoniresearch.gmail.com

---

This project demonstrates the power of **deep learning for geospatial applications**, bridging AI and remote sensing for smart urban planning and environmental monitoring.  
