# Predictive Modeling with Classical Machine Learning

**InternVision Technology Private Limited - Artificial Intelligence Internship (Minor Project)**

## 📌 Project Overview
This project focuses on foundational concepts of Machine Learning, specifically data preprocessing, model evaluation, and classical predictive modeling. The goal of this project is to build and evaluate a Logistic Regression classification model using a well-known public dataset.

## 🗄️ Dataset
* **Dataset Used:** Iris Classification Dataset (via `scikit-learn` built-in datasets)
* **Description:** The dataset contains 150 samples of Iris flowers, categorized into three species based on four features: sepal length, sepal width, petal length, and petal width.

## 🛠️ Technologies & Libraries
* **Language:** Python 3.10
* **Environment:** Anaconda, Jupyter Notebook
* **Libraries:** * `pandas` (Data Manipulation)
  * `scikit-learn` (Machine Learning & Evaluation)
  * `matplotlib` (Data Visualization)

## ⚙️ Environment Setup
To run this project locally, you need to set up a Conda environment. Run the following commands in your Anaconda prompt or terminal:

1. **Create the environment:**
   ```bash
   conda create -n internvision_ml python=3.10
   ```
2. **Activate the environment:** 
    ```
    conda activate internvision_ml
    ```
3. **Install dependencies:**
    ```
    conda install pandas scikit-learn matplotlib jupyter
    ```
## 🚀 Usage 
Open the `minor.ipynb` Jupyter Notebook in your preferred editor (like VS Code or Jupyter web interface) and run the cells sequentially. Ensure your active kernel is set to the `internvision_ml` environment.

The notebook covers:
1. Data Acquisition & Preprocessing
2. Feature ($\mathbf{X}$) and Target ($\mathbf{y}$) Separation
3. Train-Test Split (70% Training / 30% Testing)
4. Logistic Regression Model Training
5. Evaluation Metrics Calculation

## 📊 Results
The Logistic Regression model achieved perfect classification on the unseen testing data (test size = 30%, random state = 42).
- Accuracy: 1.0000
- Precision: 1.0000
- Recall: 1.0000
- F1-Score: 1.0000