# Student Loan Risk Prediction with Deep Learning

## Background

This project aims to complete the Week 18 challenge and predict the likelihood of student loan repayment using a deep learning model. 
## Files

*   **student_loans_with_deep_learning.ipynb**: Jupyter Notebook containing the complete analysis and model implementation.
*   **student_loans.csv**: Dataset used for training and evaluating the model (available at [https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv](https://static.bc-edx.com/ai/ail-v-1-0/m18/lms/datasets/student-loans.csv)).
*   **student_loans.keras**: Saved Keras model file.

## Instructions

The project is structured into four main parts, detailed below:

### Part 1: Prepare the data for use on a neural network model

1.  **Data Loading and Exploration:** The `student-loans.csv` dataset is loaded into a Pandas DataFrame. The DataFrame is reviewed to identify potential features and the target variable.
2.  **Feature and Target Definition:** The features (X) dataset is created using all columns except "credit\_ranking", which is used to define the target (y) dataset.
3.  **Data Splitting:**  The features and target datasets are split into training and testing sets using `train_test_split` from Scikit-learn.
4.  **Data Scaling:**  Scikit-learn's `StandardScaler` is used to scale the feature data to ensure optimal model performance.

### Part 2: Compile and Evaluate a Model Using a Neural Network

1.  **Model Creation:** A deep neural network is created using TensorFlow's Keras. The model architecture includes:
    *   Input layer with 11 features
    *   Two hidden layers with ReLU activation functions
    *   Output layer with a sigmoid activation function for binary classification
2.  **Model Compilation:** The model is compiled with the following configurations:
    *   Loss function: `binary_crossentropy`
    *   Optimizer: `adam`
    *   Metrics: `accuracy`
3.  **Model Training:** The model is trained using the training data for 50 epochs.
4.  **Model Evaluation:** The model is evaluated using the testing data to determine the loss and accuracy.
5.  **Model Saving:** The trained model is saved as `student_loans.keras`.

### Part 3: Predict loan repayment success by using your neural network model

1.  **Model Reloading:**  The saved `student_loans.keras` model is reloaded.
2.  **Prediction Generation:** Predictions are made on the testing data using the reloaded model.  The predictions are rounded to binary values (0 or 1).
3.  **Performance Evaluation:** A classification report is generated using the predictions and the testing data to evaluate the model's performance.

### Part 4: Discuss creating a recommendation system for student loans

1.  **Data Collection:** To build a recommendation system for student loan options, the following data would be relevant:
    *   **Student Data:** Age, location, current income, credit score, GPA, and academic information.
    *   **Loan Data:** Interest rates, repayment terms, eligibility requirements, and lender information.
    *   **Relevance:** This data helps match students with loans they qualify for, can afford, and offer the best terms.
2.  **Filtering Method:** Content-based filtering is suitable for this recommendation system. It analyzes the student's profile (finances, academics) and matches them to loan characteristics (interest, terms).
3.  **Real-World Challenges:**
    *   **Data Privacy:** Acquiring data while adhering to privacy regulations (e.g., FERPA) is crucial.
    *   **Bias Mitigation:** Ensuring the system doesn't perpetuate discriminatory lending practices from historical data is essential for fairness.

## Technologies Used

*   Python
*   Pandas
*   Scikit-learn
*   TensorFlow
*   Keras
