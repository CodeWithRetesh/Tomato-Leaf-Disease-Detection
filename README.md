# 🍅 Tomato Leaf Disease Detection using ResNet18

A Deep Learning project that detects tomato leaf diseases using a **ResNet18 Convolutional Neural Network** built with **PyTorch**.

This model classifies tomato leaf images into multiple disease categories and healthy leaves.

---

## 📊 Dataset

Dataset used in this project:
```
https://www.kaggle.com/datasets/shylesh101/tomato-leaf-disease
```
The dataset contains images of tomato leaves belonging to the following classes:
```
• Tomato Bacterial Spot
• Tomato Early Blight
• Tomato Healthy
• Tomato Late Blight
• Tomato Leaf Mold
• Tomato Septoria Leaf Spot
• Tomato Spider Mites
• Tomato Target Spot
• Tomato Mosaic Virus
• Tomato Yellow Leaf Curl Virus
```
---

## 🧠 Model Architecture

This project uses **ResNet18** with **Transfer Learning**.

Steps followed:

1. Load pretrained ResNet18
2. Freeze initial layers
3. Replace final fully connected layer
4. Train model on tomato dataset
5. Save trained model as `.pth`

---

## 📁 Project Structure

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

## ⚙️ Installation

Clone the repository

```
git clone https://github.com/CodeWithRetesh/Tomato-Leaf-Disease-Detection.git
```

Move into the project folder

```
cd Tomato-Leaf-Disease-Detection
```

Install dependencies

```
pip install -r requirements.txt
```

---

## 🚀 Running Inference

Open the notebook:

```
notebook/Inference.ipynb
```

Upload a tomato leaf image and the model will predict the disease class.

---

## 📈 Technologies Used

* Python
* PyTorch
* Torchvision
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

## 🎯 Future Improvements

* Deploy using **Streamlit Web App**
* Add **Grad-CAM visualization**
* Add **real-time disease detection**
* Create **mobile-friendly UI**

---

## 👨‍💻 Author
```
Retesh Halder
B.Tech Information Technology Student
AI / Machine Learning Enthusiast
```
