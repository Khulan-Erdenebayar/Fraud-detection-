# Credit Card Fraud Detection Project

## Project Overview
This project aims to detect fraudulent credit card transactions using machine learning models. The **Credit Card Fraud Detection Dataset** provides a clean and preprocessed dataset that includes anonymized features transformed using PCA. The focus is on building efficient and accurate models to identify fraud while minimizing false positives, leveraging the simplicity of the dataset to experiment with various machine learning techniques.

## Dataset Description
The Credit Card Fraud Detection dataset contains:
- **Total Transactions:** 284,807
- **Fraud Proportion:** ~0.172% (492 fraud cases)
- **Features:** 30 numerical features transformed using PCA, along with:
  - `Time`: Seconds since the first transaction.
  - `Amount`: Transaction amount.
  - `Class`: Target variable (0 = Legitimate, 1 = Fraud).
- **Missing Data:** None.

### Characteristics
1. **Class Imbalance:** Fraudulent transactions are rare (~0.172%), making it crucial to use techniques to handle imbalance.
2. **Anonymized Features:** All features are numerical and transformed using PCA, providing no direct interpretability.
3. **Clean Dataset:** No missing data, simplifying preprocessing steps.

## Objectives
1. Explore the dataset and identify patterns distinguishing fraud from legitimate transactions.
2. Handle the class imbalance using appropriate techniques.
3. Build machine learning models to accurately detect fraudulent transactions.
4. Evaluate model performance using metrics suitable for imbalanced datasets.

## Workflow
1. **Data Preprocessing:**
   - Scaled `Time` and `Amount` features using standardization.
   - No imputation needed as the dataset contains no missing values.

2. **EDA (Exploratory Data Analysis):**
   - Visualized the distribution of `Time` and `Amount` for fraud and non-fraud cases.
   - Examined the class imbalance and its implications on model training.
   - Analyzed correlation between PCA-transformed features to understand data structure.

3. **Model Development:**
   - Tested various machine learning models, including Random Forest, XGBoost, LightGBM, and Logistic Regression.
   - Addressed class imbalance using:
     - Class weighting in models to give higher importance to fraud cases.
   - Hyperparameter tuning for optimized performance.

4. **Evaluation Metrics:**
   - F1-Score (for balancing precision and recall).
   - Precision and recall to measure fraud detection accuracy.
   - AUC (Area Under the Curve) to evaluate model effectiveness.

## Key Findings
- **Fraud Patterns:**
  - Fraudulent transactions often have smaller amounts compared to legitimate ones.
  - Fraudulent transactions are uniformly distributed across the `Time` variable.
- **Model Performance:**
  - **XGBoost:** Achieved the highest F1-Score of 0.877, balancing precision and recall effectively.
  - **Random Forest:** Performed well but slightly behind XGBoost.
  - **Logistic Regression:** Good baseline but struggled with imbalanced data.
  - **CatBoost:** Balanced performance with minimal feature preprocessing.

## Tools and Libraries
- Python, Pandas, NumPy, Scikit-learn
- XGBoost, LightGBM, CatBoost
- Matplotlib, Seaborn for visualization


## Future Directions
1. Experiment with ensemble methods combining multiple models to improve detection.
2. Investigate deep learning models, such as autoencoders, for anomaly detection.
3. Extend the analysis by introducing additional synthetic features or external datasets.
4. Explore cost-sensitive learning to minimize the financial impact of fraud.

## References
The following resources were instrumental in guiding this project:
1. [Credit Fraud: Dealing with Imbalanced Datasets by janiobachmann](https://www.kaggle.com/code/janiobachmann/credit-fraud-dealing-with-imbalanced-datasets)
2. [Automatic EDA Libraries Comparison by andreshg](https://www.kaggle.com/code/andreshg/automatic-eda-libraries-comparisson)
3. [GBM vs XGBoost vs LightGBM by nschneider](https://www.kaggle.com/code/nschneider/gbm-vs-xgboost-vs-lightgbm)

---

This README provides a detailed overview of the Credit Card Fraud Detection project, its workflow, findings, and references for further exploration.
