# Fake Internship Detection Using Machine Learning

## 1. Project Overview

This project develops a machine-learning-based system for detecting potentially fake internship postings.

The original dataset contains approximately 1,000,000 internship-posting records. Due to computational and memory limitations of the available hardware, a subset of 100,000 records was used for the experimental implementation.

The project follows an end-to-end machine learning workflow, including:

- Dataset loading and auditing
- Exploratory Data Analysis (EDA)
- Data preprocessing
- Feature preparation
- Baseline model development
- Machine learning model training
- Hyperparameter tuning and validation
- Model evaluation
- Confusion matrix and error analysis
- Final model selection

## 2. Models Used

The following models were evaluated:

- Dummy Classifier (Baseline)
- Logistic Regression
- Decision Tree
- Random Forest

The final model is selected based on the experimental results using metrics such as accuracy, precision, recall, F1-score, confusion matrix results, validation performance, and computational requirements.

## 3. Dataset

### Original Dataset

The original dataset contains approximately:

- Number of records: 1,000,000
- Task: Binary classification
- Target: Fake/Genuine internship posting

### Experimental Dataset

For this project, 100,000 records were used because of the computational limitations of the available laptop.

The dataset should be placed in the project data directory:

    data/

For example:

    data/fake_internship_detection_dataset.csv

## 4. Project Structure

    Fake-Internship-Detection/
    │
    ├── Dataset/
    │   └── fake_internship_detection_dataset.csv
    │
    ├── fake_internship_detection.ipynb
    │   
    │
    ├── results/
    │   ├── figures/
    │   └── visuals/
    │
    ├── requirements.txt
    ├── README.md

## 5. Requirements

The project requires Python and the following major libraries:

- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn

The exact package versions are provided in `requirements.txt`.

## 6. Environment Setup

Create a Python virtual environment:

    python -m venv venv

Activate the environment on Windows:

    venv\Scripts\activate

Install the required packages:

    pip install -r requirements.txt

## 7. Running the Project

### Option 1: Jupyter Notebook

Start Jupyter Notebook:

    jupyter notebook

Open the notebook:

    notebooks/fake_internship_detection.ipynb

Run all cells from beginning to end.

### Option 2: Google Colab

The notebook can also be executed using Google Colab.

Upload the dataset to the appropriate location and update the dataset path in the notebook if necessary.

Run the notebook cells sequentially from the beginning.

## 8. Expected Output

Running the notebook should generate:

- Dataset summary and data-quality information
- Exploratory data analysis results
- Data preprocessing results
- Baseline model performance
- Model training results
- Validation/tuning results
- Test-set evaluation metrics
- Confusion matrices
- Classification reports
- Model comparison results
- Error analysis
- Final selected model

## 9. Evaluation Metrics

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- False Positive (FP)
- False Negative (FN)
- Error Rate

Multiple metrics are used because the dataset contains an unequal distribution of genuine and potentially fake internship postings.

## 10. Reproducibility

To reproduce the results:

1. Install the required Python packages using `requirements.txt`.
2. Place the dataset in the specified `data/` directory.
3. Open the provided notebook.
4. Run the notebook from the first cell to the last cell.
5. Ensure that the same random states and preprocessing steps are used.
6. The generated tables and figures should be reproducible from the provided code.

## 11. Responsible Use

The model should be treated as a preliminary screening and decision-support tool.

A prediction of "fake" does not provide definitive proof that an internship posting is fraudulent. Model predictions should be followed by human verification.

The system should not automatically reject applications, blacklist organizations, or make irreversible decisions solely based on model predictions.

## 12. Future Improvements

Future improvements may include:

- Using the complete 1-million-record dataset
- Testing on independently collected internship postings
- Evaluating the model across different internship platforms
- Adding more recent internship data
- Improving label quality through expert verification
- Optimizing the classification threshold
- Testing additional boosting models such as Gradient Boosting and XGBoost
- Applying explainable machine-learning techniques
- Evaluating performance under distribution shift
- Developing a real-time internship screening application
