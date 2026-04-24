# 🔢 MNIST Handwritten Digit Classification

## 📄 Project Summary (Version Française)
Ce projet explore l'application de diverses techniques d'apprentissage automatique (Machine Learning) pour classifier les chiffres manuscrits de la célèbre base de données MNIST. L'étude compare des modèles linéaires comme la **Régression Logistique** à des architectures plus complexes comme le **Réseau de Neurones (LeNet-5)**. En optimisant les hyperparamètres et en utilisant l'augmentation de données, le modèle final a atteint une précision de **99,17 %**, démontrant l'efficacité du Deep Learning pour la reconnaissance optique de caractères (OCR).

---

## 📌 Project Overview
This report investigates five machine learning algorithms to classify handwritten digits (0–9) from the MNIST dataset (70,000 images). The goal is to balance accuracy, computational efficiency, and scalability.

**Models Investigated:**
* Logistic Regression (LR)
* Linear Discriminant Analysis (LDA)
* Decision Tree (DT)
* Random Forest (RF)
* Neural Network (NN)

## 🛠 Methodology & Technical Toolkit
* **Preprocessing:** Min-Max Scaling was applied to normalize pixel intensities to a $[0,1]$ range.
* **Validation:** Used **5-fold cross-validation** to determine the mean accuracy across different data subsets.
* **Deep Learning Optimization:** * **Architecture:** Modified **LeNet-5** with ReLU activations and Dropout (25%) to prevent overfitting.
    * **Data Augmentation:** Random rotations ($10^\circ$), zooms (10%), and shifts.
    * **Scheduler:** Variable learning rate scheduler (factor of 0.2) to refine convergence.

## 📊 Performance Results

| Model | Validation Accuracy (%) |
| :--- | :--- |
| Logistic Regression | 92.0% |
| Linear Discriminant Analysis | 86.3% |
| Decision Tree | 86.8% |
| Random Forest | 96.7% |
| **Neural Network (Optimized)** | **99.17%** |

## 🔍 Key Insights
* **Confusion Matrix:** Analysis showed that misclassifications often occur between similar digits like **3 and 5** or **4 and 9**.
* **Complexity vs. Accuracy:** While Random Forest performed remarkably well for its simplicity, the Neural Network's ability to handle non-linear patterns made it the superior choice for high-precision tasks.

## 📂 Project Assets
* **Model Script:** `mnist_model.py` (PyTorch implementation)
* **Notebook:** `MNIST_Analysis.ipynb`
* **Dataset:** Accessed via `scikit-learn` (fetch_openml)

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies: `pip install torch torchvision scikit-learn matplotlib`.
3. Run the notebook to view the training logs and confusion matrix.

---
**By: Yuanyuan (Coco) Wei** | *Maths & Stats Graduate* | 📍 Montreal, QC
