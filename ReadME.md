# **Credit Card Default Prediction using Deep Learning Models**

This repository provides a deep learning methodology for predicting the likelihood of a credit card holder defaulting on payments. The project demonstrates advanced techniques in data preprocessing, neural network modeling, and ensemble learning using Python and TensorFlow/Keras. The final model enhances accuracy by combining multiple predictions.

---

## **Key Features of the Project**

1. **Data Preprocessing**  
   - Efficient handling of missing values, normalization, and class balancing.

2. **Multiple Model Architectures**  
   - Development of distinct models:  
     - **Multilayer Perceptron (MLP)** for general tabular data.  
     - **Recurrent Neural Networks (RNNs)** to capture sequential patterns.

3. **Ensemble Learning**  
   - Stacking multiple models to create a final predictive model.

4. **Performance Metrics**  
   - Evaluation using accuracy and loss metrics, with visualizations to track training performance.

---

## **Project Overview**

### 1. Data Preprocessing
- Loaded data from an Excel file.
- Dropped descriptive rows and converted the target variable to integer type.
- Created train-validation splits for both MLP and RNN models.

---

### 2. MLP Model
The MLP model consists of:
- **Input layer** with 300 units and ReLU activation.
- Multiple **hidden layers** with dropout for regularization.
- Final layer with **sigmoid activation** for binary classification.
- Compiled using the **Adam optimizer** with a learning rate of 0.015.
- Trained for **18 epochs** with class weights to handle imbalanced data.

---

### 3. RNN Models
Two RNN models were developed:
- Each model uses two **LSTM layers** followed by a **dense layer** with sigmoid activation.
- Compiled using the **Adam optimizer** with a learning rate of 0.0001.
- Trained for **20 epochs** with class weights.

---

### 4. Ensemble Model
- Combined predictions from the MLP and RNN models into an ensemble model.
- The ensemble model architecture includes:
  - A **dense layer** with ReLU activation.
  - **Dropout** for regularization.
  - Final **output layer** with sigmoid activation.
- Trained for **20 epochs** using the combined predictions as input.

---

## **Results**

### **Training Performance**
- The MLP and RNN models were evaluated on the validation set, showing reasonable accuracy.
- The ensemble model achieved the best accuracy, demonstrating the strength of combining multiple models.

