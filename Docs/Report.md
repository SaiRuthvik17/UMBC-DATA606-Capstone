1. Title and Author
Project Title: Loan Eligibility Prediction

Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie (Jay) Wang

Author Name: Sai Ruthvik Anantapalli

Link to the author's GitHub profile: https://github.com/SaiRuthvik17

Link to the author's LinkedIn profile: www.linkedin.com/in/sai-ruthvik-anantapalli-884b43227

2. Background
What is it about?

The project focuses on predicting loan eligibility for individuals applying for loans. Using machine learning models, it aims to analyze various applicant details, such as demographic information, financial history, and loan requirements, to determine the likelihood of loan approval. The dataset includes variables like Gender, Marital Status, Education, Employment Status, Applicant and Coapplicant Income, Loan Amount and Term, Credit History, Property Area, and the Loan Status (approved or denied). The goal is to assist lenders in making informed decisions about loan approvals and to potentially streamline the application process for both lenders and applicants.

Why does it matter?

Accurately predicting loan eligibility matters significantly for a multitude of reasons, encompassing efficiency, objectivity, risk management, and financial inclusion. By harnessing predictive models, financial institutions can streamline the loan application process, enhancing operational efficiency by reducing the time and resources required for manual assessments. This automation not only aids in achieving greater objectivity in lending decisions—minimizing human bias—but also plays a crucial role in risk management by identifying applicants likely to default, thereby safeguarding against financial losses. Moreover, these predictive capabilities extend the benefits of financial products to underserved communities, promoting financial inclusion by enabling access to credit for a broader spectrum of individuals. Together, these factors contribute to a more equitable, efficient, and secure lending landscape, underscoring the profound impact of accurate loan eligibility predictions on both the micro and macroeconomic scales.

What are your research questions?

What all factors (or) attributes most significantly influence the loan approval decisions?

How does applicant's and co-applicant's income level affect the loan eligibility?

How can the credit history attribute play in determining loan acceptance?

How will the different categories of property area reflect on loan approval?

3. Data
Data sources: https://www.kaggle.com/datasets/vikasukani/loan-eligible-dataset?select=loan-test.csv

Data size: 60kb

Data shape:

loan-train : 614 rows and 13 columns

loan-test: 367 rows and 12 columns

What does each row represent?

Each row represents a loan application details submitted by each individual. This consists of different categories and requirements for the approval of loan.

Data dictionary

Columns Name	Data Type	Definition	Potential Values
Loan_ID	Object	Unique loan application identifier	LP001002, LP001003, ...
Gender	Object	The gender of the applicant	Male, Female
Married	Object	Marital status of the applicant	Yes, No
Dependents	Object	Number of dependents the applicant has	0, 1, 2, 3+
Education	Object	The highest education level of the applicant	Graduate, Not Graduate
Self_Employed	Object	Self-employment status of the applicant	Yes, No
ApplicantIncome	Int64	Monthly income of the applicant	Continuous values
CoapplicantIncome	Float64	Monthly income of the co-applicant	Continuous values
LoanAmount	Float64	Loan amount in thousands	Continuous values
Loan_Amount_Term	Float64	Term of loan in months	360, 120, etc.
Credit_History	Float64	Credit history meets guidelines	1 (Yes), 0 (No)
Property_Area	Float64	Type of the property area	Urban, Rural, Semiurban
Loan_Status	Object	Loan approval status	Y (Yes), N (No)
Which variable/column will be your target/label in your ML model?

Loan_Status: This is the variable you would predict, indicating whether a loan is approved (Y) or denied (N).

Which variables/columns may be selected as features/predictors for your ML models?

Credit_History: This is a key indicator of a borrower's reliability and past loan repayment behavior. A positive credit history suggests a higher probability of timely loan repayments, making it a critical factor in loan approval decisions.

ApplicantIncome: This reflects the applicant's ability to repay the loan. Higher income levels generally increase the likelihood of loan approval as they indicate greater financial stability and repayment capacity.

LoanAmount: This determines the risk associated with the loan. Larger loan amounts may be perceived as higher risk, affecting the approval decision. The amount requested needs to be within reasonable limits based on the applicant's income.

CoapplicantIncome: This enhances the assessment of repayment capacity. The inclusion of a coapplicant's income can significantly increase the total income considered for loan repayment, potentially offsetting risks associated with lower primary applicant incomes.

Education: This indicates the applicant's level of education, which can be a proxy for earning potential and financial literacy. Applicants with higher education levels may be perceived as having better employment prospects and stability, potentially influencing loan approval positively.

4. Exploratory Data Analysis(EDA)

Performed data exploration using Jupyter Notebook, focused on the target variable ('Loan_Status') and selected the required features and dropping all other columns. Produced a summary statistics of key variables and created visualization using MatplotLib to gain valuable insights into the dataset. Addtionally, investigated if the data required any cleaning, such as handling missing values and duplicate rows. Here are the key findings:

Summary statistics revealed insights into the distribution of numerical variables such as ApplicantIncome, CoapplicantIncome, and LoanAmount.
Visualizations provided a graphical representation of the distribution of variables and potential relationships between them.
Observed missing values in columns such as Gender, Married, Dependents, Self_Employed, Loan_Amount_Term, Credit_History, and LoanAmount. These missing values were imputed using median and mode methods.
No duplicate rows were found in the dataset.

5. Model Training

For this predictive analytics, three models were used to train and test the data:

Random Forest Classifier: A powerful ensemble learning technique capable of handling both numerical and categorical data.
Logistic Regression: A simple and effective classification algorithm suitable for binary outcome prediction tasks.
Simple Vector Machine:

We trained the models using the train-test split method with a split ratio of 70/30. The Python packages utilized included scikit-learn for model training and evaluation. The development environment used was Jupyter Notebook running on a local machine.

Model performance was evaluated based on metrics such as accuracy, precision, recall, and F1-score. These metrics were used to compare the performance of different models and select the best-performing one for deployment.

6. Application of the Trained Model

Developed a web application using Streamlit to allow the users to interact with the trained models. This web application enables individuals to input their applicant details and receive predictions regarding their loan-eligibility in real-time. By providing a user-friendly interface, this aims to make loan approval process more accessible and transparent to both lenders and applicants.

7. Conclusion

In conclusion, this project aims to address the critical need for accurate loan eligibility predictions using machine learning techniques. By leveraging predictive models trained on historical loan data, financial institutions can streamline the lending process, improve decision-making, and promote financial inclusion. While this current analysis provides valuable insights into loan approval factors and model performance, there are limitations to consider, including the availability and quality of data, model interpretability, and potential biases. Moving forward, future research could focus on refining the models, incorporating additional data sources, using live data to train the model, and exploring advanced machine learning techniques to further enhance predictive accuracy and fairness in lending practices.

8. References:
