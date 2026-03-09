#  Tomato Leaf Disease Detection using Deep Learning (ResNet18)

## Overview :
Plant diseases are one of the major reasons for crop loss in agriculture. Early detection of leaf diseases can significantly help farmers take timely action and protect crop yield.

This project focuses on detecting **tomato leaf diseases using a deep learning model**. A Convolutional Neural Network based on **ResNet18 architecture** was trained to classify different types of tomato leaf diseases from images.

The model learns visual patterns such as discoloration, spots, and texture changes on leaves and predicts the disease category automatically.

The implementation is built using **PyTorch** and supports both **CPU and GPU (CUDA)** execution.

 
## Dataset :

The dataset used in this project comes from Kaggle.

Dataset Link:
https://www.kaggle.com/datasets/shylesh101/tomato-leaf-disease

The dataset contains images of tomato leaves belonging to the following classes:
```
* Tomato Bacterial Spot
* Tomato Early Blight
* Tomato Healthy
* Tomato Late Blight
* Tomato Leaf Mold
* Tomato Septoria Leaf Spot
* Tomato Spider_mites Two-spotted_spider_mite
* Tomato Target Spot
* Tomato Mosaic Virus
* Tomato Yellow Leaf Curl Virus
```
The dataset is organized into **training, validation, and testing folders**, where each class is stored in its own directory.

Due to the dataset's large size, it is not included in this repository. Users are expected to download it directly from the source and place it in the appropriate folder structure.

---

## Model Architecture :

The model used in this project is **ResNet18**, a deep residual network widely used for image classification tasks.

Key details:
```
Base Model: ResNet18
Pretrained Weights: ImageNet
Framework: PyTorch
Training Method: Transfer Learning
```
The final fully connected layer of ResNet18 was modified to classify **10 disease categories**.

---

## Training Details :
 
The model was trained with the following configuration:
```
Input Image Size: 224 × 224
Batch Size: 32
Epochs: 25

Loss Function: CrossEntropyLoss

Optimizer: Stochastic Gradient Descent (SGD)
Learning Rate: 0.001
Momentum: 0.9

Training was performed using a **CUDA-enabled GPU** for faster computation.
```
---

## Model Performance :

Final results after 25 epochs:
```
Training Loss: 0.0019
Training Accuracy: 99.97%

Validation Loss: 0.0139
Validation Accuracy: 99.56%

The model achieved very strong performance across all classes.
```
## Classification Report :

The model performance on the evaluation dataset is summarized below.

```
              precision    recall  f1-score   support

           0       1.00      1.00      1.00       425
           1       0.99      1.00      0.99       480
           2       1.00      0.99      1.00       463
           3       1.00      1.00      1.00       470
           4       1.00      1.00      1.00       436
           5       0.99      0.99      0.99       435
           6       0.99      0.99      0.99       457
           7       1.00      1.00      1.00       490
           8       1.00      1.00      1.00       448
           9       1.00      1.00      1.00       481

    accuracy                           1.00      4585
   macro avg       1.00      1.00      1.00      4585
weighted avg       1.00      1.00      1.00      4585
```

The classification report shows very high precision, recall, and F1-scores across all classes, indicating that the model can accurately distinguish between different tomato leaf diseases.


---

## Project Structure :

```
Tomato-Leaf-Disease-Detection
│
├── model
│   └── tomato_disease_model.pth
│
├── notebook
│   ├── Model.ipynb
│   └── Inference.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## Installation

Clone the repository:

```
git clone https://github.com/CodeWithRetesh/Tomato-Leaf-Disease-Detection.git
```

Navigate to the project folder:

```
cd Tomato-Leaf-Disease-Detection
```

Install required dependencies:

```
pip install -r requirements.txt
```

---

## Running Inference

Inference is demonstrated in the **Inference.ipynb** notebook.

The process includes:
```
* Loading the trained model
* Applying the same preprocessing used during training
* Passing a tomato leaf image to the model
* Predicting the disease class
```
Users can test the model by providing their own leaf images.

---

## Technologies Used
```
Python
PyTorch
Torchvision
NumPy
Pandas
Matplotlib
Scikit-learn
```
---

## Future Improvements

Possible improvements for this project include:
```
* Building a web application using Streamlit 
* Adding Grad-CAM visualization to highlight infected regions
* Creating a mobile-friendly disease detection tool for farmers
* Expanding the model to support more crop diseases
```
---

## Author
```
Retesh Halder
B.Tech Information Technology Student
AI / Machine Learning /Deep Learning Enthusiast

Interested in Artificial Intelligence, Machine Learning, and Computer Vision applications for real-world problems.

