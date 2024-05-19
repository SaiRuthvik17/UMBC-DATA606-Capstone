### Loan Eligibility Prediction

## **1. Title and Author**

* **Project Title:** Loan Eligibility Prediction
* **Prepared for:** UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang
* **Author Name:** Sai Ruthvik Anantapalli
* **Author's GitHub Profile:** [https://github.com/SaiRuthvik17](https://github.com/SaiRuthvik17)
* **Author's LinkedIn Profile:** [www.linkedin.com/in/sai-ruthvik-anantapalli-884b43227](https://www.linkedin.com/in/sai-ruthvik-anantapalli-884b43227)

## **2. Background**

**What is it about?**

This project focuses on predicting loan eligibility for loan applicants. Machine learning models analyze various details, including demographics, financial history, and loan requirements, to determine loan approval likelihood. The dataset includes variables like Gender, Marital Status, Education, Income (applicant and coapplicant), Loan Amount and Term, Credit History, Property Area, and Loan Status (approved/denied). The goal is to assist lenders in making informed decisions and potentially streamline the application process.

**Why does it matter?**

Accurate loan eligibility prediction is significant for several reasons: efficiency, objectivity, risk management, and financial inclusion. Predictive models can streamline the process, reduce manual assessment time and resources. This automation promotes objectivity in lending decisions and risk management by identifying potential defaulters. Additionally, these capabilities extend financial products to underserved communities, promoting financial inclusion. These factors contribute to a more equitable, efficient, and secure lending landscape.

**Research Questions**

* What factors most significantly influence loan approval decisions?
* How does applicant/co-applicant income affect loan eligibility?
* How does credit history impact loan acceptance?
* How do property area categories affect loan approval?

## **3. Data**

**Data Source:** [https://www.kaggle.com/datasets/vikasukani/loan-eligible-dataset?select=loan-test.csv](https://www.kaggle.com/datasets/vikasukani/loan-eligible-dataset?select=loan-test.csv)

**Data Size:** 60kb

**Data Shape**

* loan-train: 614 rows, 13 columns
* loan-test: 367 rows, 12 columns

**What does each row represent?**

Each row represents a loan application with details submitted by an individual. These details include various categories and requirements for loan approval.

**Data Dictionary**

| Column Name | Data Type | Definition | Potential Values |
|---|---|---|---|
| Loan_ID | Object | Unique loan application identifier | LP001002, LP001003, ... |
| Gender | Object | The gender of the applicant | Male, Female |
| Married | Object | Marital status of the applicant | Yes, No |
| Dependents | Object | Number of dependents the applicant has | 0, 1, 2, 3+ |
| Education | Object | The highest education level of the applicant | Graduate, Not Graduate |
| Self_Employed | Object | Self-employment status of the applicant | Yes, No |
| ApplicantIncome | Int64 | Monthly income of the applicant | Continuous values |
| CoapplicantIncome | Float64 | Monthly income of the co-applicant | Continuous values |
| LoanAmount | Float64 | Loan amount in thousands | Continuous values |
| Loan_Amount_Term | Float64 | Term of loan in months | 360, 120, etc. |
| Credit_History | Float64 | Credit history meets guidelines | 1 (Yes), 0 (No) |
| Property_Area | Float64 | Type of the property area | Urban, Rural, Semiurban |
| Loan_Status | Object | Loan approval status | Y (Yes), N (No) |

**Target Variable/Label**

* Loan_Status: This variable indicates loan approval (Y) or denial (N).

**Features/Predictors**

* Credit_History: Indicates borrower reliability and past loan repayment behavior.
* ApplicantIncome: Reflects the applicant's ability to repay the loan.
* LoanAmount: Determines the risk associated with the loan.
* CoapplicantIncome: Enhances the assessment of repayment capacity.
* Education: A proxy for earning potential and financial literacy.

## **4. Exploratory Data Analysis (EDA)**

* Performed using Jupyter Notebook, focusing on the target variable ('Loan_Status') and selected features.
* Created summary statistics of key variables and visualizations using MatplotLib to gain insights.
* Investigated missing values and duplicate rows.
    * Summary statistics revealed insights into numerical variable distributions.
    * Visualizations provided a graphical representation of variable distributions and potential relationships.
    * Missing values were found in some columns and imputed using median/mode methods.
    * No duplicate rows were found.

## **5. Model Training**

Three machine learning models were used to train and test the data:

* **Random Forest Classifier:** A powerful ensemble learning technique that can handle both numerical and categorical data.
* **Logistic Regression:** A simple and effective classification algorithm suitable for binary outcome prediction tasks like loan eligibility.
* **Support Vector Machine (SVM):** A powerful model for classification tasks, known for its ability to handle high-dimensional data.

**Training Process:**

* The train-test split method was used with a 70/30 split ratio, dividing the data into training and testing sets.
* Python libraries like scikit-learn were used for model training and evaluation.
* The development environment was Jupyter Notebook running on a local machine.

**Model Evaluation:**

* Performance was evaluated using metrics like accuracy, precision, recall, and F1-score. 
* These metrics helped compare model performance and select the best model for deployment.

## **6. Application of the Trained Model**

A web application was developed using Streamlit to allow users to interact with the trained model. This application enables individuals to input their loan application details and receive real-time predictions regarding their loan eligibility. The user-friendly interface aims to make the loan approval process more accessible and transparent for both lenders and applicants.

## **7. Conclusion**

This project highlights the importance of accurate loan eligibility prediction using machine learning. Predictive models trained on historical loan data can streamline the lending process, improve decision-making for financial institutions, and promote financial inclusion. While this analysis provides valuable insights, there are limitations to consider, such as:

* **Data Availability and Quality:** The quality and representativeness of the data used can impact model performance. 
* **Model Interpretability:** Understanding how models arrive at predictions can be challenging, limiting their transparency.
* **Potential Biases:** Biases present in the data can lead to biased model predictions.

**Future Research Directions:**

* Refining the models through hyperparameter tuning and feature engineering.
* Incorporating additional data sources for potentially richer insights.
* Utilizing live data to continuously train and improve the model's performance.
* Exploring advanced machine learning techniques for further enhanced predictive accuracy and fairness in lending practices.

## **8. References**


