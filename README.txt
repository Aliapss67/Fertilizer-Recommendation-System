# Fertilizer Recommendation System

---

## Overview

This project develops a machine learning model designed to recommend the top 3 most suitable **fertilizers** for various **agricultural conditions**. By analyzing diverse environmental and soil parameters, the system aims to provide accurate predictions, thereby optimizing crop yield and enhancing agricultural efficiency.

---

## Features

* **Data Preprocessing:** Robust handling of raw agricultural datasets, including cleaning, formatting, and preparing data for model training.
* **Feature Engineering:** Creation of new, insightful features from existing data to improve model performance. This includes interactive and ratio-based features.
* **Machine Learning Model:** Utilizes **LightGBM**, a highly efficient gradient boosting framework, for multi-class classification.
* **Hyperparameter Tuning:** Employs **RandomizedSearchCV** to find the optimal set of model parameters, enhancing predictive accuracy.
* **Model Evaluation:** Performance is rigorously assessed using **Mean Average Precision at K (MAP@3)**, a key metric for ranking-based recommendations.
* **Cross-Validation:** Implements **K-Fold Cross-Validation** for more reliable model evaluation and to ensure better generalization to unseen data.
* **Submission Ready:** Generates a `submission.csv` file in the format required for Kaggle competitions.

---

## Project Structure

The project is typically structured as a Jupyter Notebook (`.ipynb` file) containing sequential cells for data processing, model training, and evaluation. Key steps include:

1.  **Environment Setup & Data Loading:** Importing libraries and loading `trainaa.csv` and `testaa.csv`.
2.  **ID Management:** Separating and storing `id` columns from test data for submission purposes.
3.  **Exploratory Data Analysis (EDA):** Initial data insights and visualization.
4.  **Data Preprocessing:** Handling categorical variables (e.g., using One-Hot Encoding).
5.  **Feature Engineering:** Creating new features to enhance model learning.
6.  **Data Splitting:** Preparing data into training and validation sets.
7.  **Model Training:** Initial LightGBM model training.
8.  **Hyperparameter Tuning:** Using `RandomizedSearchCV` to fine-tune the model.
9.  **Cross-Validation:** Robust evaluation of the best model using `StratifiedKFold`.
10. **Prediction & Submission:** Generating predictions on the test set and creating `submission.csv`.

---

## How to Use (Local Setup)

To run this project locally, follow these steps:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/YourGitHubUsername/Fertilizer-Recommendation-System.git](https://github.com/YourGitHubUsername/Fertilizer-Recommendation-System.git)
    cd Fertilizer-Recommendation-System
    ```
    (Replace `YourGitHubUsername` and `Fertilizer-Recommendation-System` with your actual username and repository name if different).

2.  **Install Dependencies:**
    It's recommended to use a virtual environment.
    ```bash
    pip install pandas numpy scikit-learn lightgbm
    ```
    (You might also need `ipykernel` for Jupyter Notebook: `pip install ipykernel`)

3.  **Download Data:**
    Obtain `trainaa.csv` and `testaa.csv` from the relevant Kaggle competition or data source and place them in the project's root directory (or update the file paths in the notebook's first cell).

4.  **Run Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    Open the `.ipynb` file (e.g., `Fertilizer_Recommendation_Notebook.ipynb`) and run all cells sequentially.

---

## Results & Performance

The model's performance is primarily measured by **Mean Average Precision at K (MAP@3)**. After hyperparameter tuning and cross-validation, the model aims to achieve a competitive score on benchmark datasets like Kaggle. The `submission.csv` file generated can be directly uploaded to relevant platforms for evaluation.

---

## Contributing

Feel free to fork this repository, submit pull requests, or open issues. Any contributions to improve the model's accuracy, efficiency, or documentation are welcome!

---

## License

This project is open-source and available under the [MIT License](https://opensource.org/licenses/MIT).

---