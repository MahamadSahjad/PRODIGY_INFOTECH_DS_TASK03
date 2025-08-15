# PRODIGY_INFOTECH_DS_TASK03
Decision Tree Classifier built using the UCI Bank Marketing dataset to predict customer purchase likelihood, with preprocessing, hyperparameter tuning, evaluation, and visualizations.
# Decision Tree Classifier - Bank Marketing Dataset

This project uses a **Decision Tree Classifier** to predict if a customer will purchase a product or service. The prediction is based on **demographic data** (age, job, education, etc.) and **behavioral data** (previous marketing interactions, contact duration, etc.) from the **UCI Bank Marketing Dataset**.

---

## Steps in the Project

### 1. Load the dataset from UCI or a local file
We first load the **bank marketing dataset**.  
- If the dataset is available locally, we load it from the computer.  
- If not, it is automatically downloaded from the **UCI Machine Learning Repository**.

### 2. Preprocess data (scale numbers, encode categories)
The raw dataset contains both **numeric** (e.g., age, campaign duration) and **categorical** (e.g., job type, marital status) data.  
- **Numeric data** is standardized using `StandardScaler` so values have similar scales.  
- **Categorical data** is converted into numeric format using `OneHotEncoder`.

### 3. Build and train the Decision Tree model
We create a **machine learning pipeline** that combines preprocessing with the Decision Tree Classifier.  
This ensures that data is always prepared in the same way before training or prediction.

### 4. Tune hyperparameters using GridSearchCV
We test multiple **Decision Tree settings** to find the best performing model.  
Parameters tested include:
- Splitting criterion (`gini` or `entropy`)
- Maximum depth of the tree
- Minimum samples required to split a node

We use **5-fold cross-validation** to get reliable results.

### 5. Evaluate the model
We measure performance using:
- **Accuracy** – how many predictions are correct
- **Classification Report** – includes precision, recall, and F1-score
- **Confusion Matrix** – shows correct and incorrect predictions in a table format

### 6. Visualize results
We create visual charts to better understand the model:
- **Confusion Matrix** heatmap
- **Feature Importance Chart** showing the most important variables
- **Partial Decision Tree Plot** to view the top few levels of the tree

### 7. Save the trained model for future use
The final model is saved as a `.joblib` file so it can be loaded later without retraining.

---

## Tools Used
- **Python** – programming language
- **Pandas, NumPy** – data handling
- **Scikit-learn** – machine learning models and preprocessing
- **Matplotlib** – plotting and visualization

---

## How to Run
1. Clone this repository to your local machine.  
2. Install all required libraries using:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the Jupyter Notebook file and run all cells:
   ```bash
   jupyter notebook Decision_Tree_Bank_Marketing.ipynb
   ```
