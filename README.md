# Pixel Coordinate Prediction Using CNN (Supervised Regression)

## 📌 Problem Statement
The objective of this project is to predict the (x, y) coordinates of a single white pixel (pixel value = 255) present in a 50×50 grayscale image, where all other pixels have a value of 0. The pixel location is randomly generated for each image. This is a supervised regression problem solved using Deep Learning.

---

## 📊 Dataset Generation
Since no real dataset is provided, a synthetic dataset was generated:

- Image Size: 50 × 50 (Grayscale)
- Total Samples: 10,000
- Each image contains:
  - One randomly placed white pixel (value = 255)
  - All other pixels are black (value = 0)
- Labels:
  - Corresponding (x, y) coordinates of the white pixel

### Dataset Split:
- Training Set: 80% (8000 samples)
- Testing Set: 20% (2000 samples)

---

## 🧠 Model Architecture (CNN Regression)

A custom Convolutional Neural Network (CNN) regression model was designed using the Keras Sequential API.

### Architecture:
- Input: 50×50×1 image
- Conv2D (16 filters, 3×3) + ReLU
- MaxPooling (2×2)
- Conv2D (32 filters, 3×3) + ReLU
- MaxPooling (2×2)
- Flatten
- Dense (64 neurons) + ReLU
- Dense (2 neurons) → Output (x, y)

### Compilation:
- Optimizer: Adam  
- Loss Function: Mean Squared Error (MSE)  
- Metric: Mean Absolute Error (MAE)

---

## 📈 Training Results
- Training and validation loss decrease rapidly and stabilize near zero.
- No signs of overfitting or underfitting.
- The model generalizes very well on unseen test data.

---

## 🖼️ Prediction Visualization
Predicted pixel coordinates closely overlap the ground truth pixel locations with sub-pixel accuracy. Most predictions differ from actual values by less than 1 pixel.

---

## 🛠️ Installation & Setup

### 1. Create Virtual Environment

### 2. Activate Environment

### 3. Install Dependencies

---

## ▶️ How to Run
1. Open the notebook:
2. Run all cells step by step:
   - Dataset Generation
   - Preprocessing
   - Model Training
   - Loss Graph
   - Prediction Visualization

---

## ✅ Conclusion
The CNN regression model successfully learns the spatial location of the white pixel and predicts (x, y) coordinates with very high accuracy. The approach satisfies all the requirements of the assignment.

---

## 👤 Author
Ashin K
