## **Problem Overview**
- This project focuses on analyzing customer behavior in the telecom industry to predict churn and identify meaningful customer segments. Using classical machine learning techniques, the goal is to build predictive models that classify customers into churn or non-churn categories and segment them into groups based on shared characteristics. This analysis will empower telecom businesses to improve customer retention and tailor services to different customer segments.


- There are 21 variables and 7043 observations in the dataset. 
    - customerID - A customer’s ID

1. demographic variables:
    - gender - A customer’s gender
    - SeniorCitizen - Whether the customer is a senior citizen or not (1, 0)
    - Partner- Whether the customer has a partner or not (Yes, No)
    - Dependents - Whether the customer has dependents or not (Yes, No)

2. variables related to the company’s services:
    - PhoneService - Whether the customer has a phone service or not (Yes, No)
    - MultipleLines - Whether the customer has multiple lines or not (Yes, No, No phone service)
    - InternetService - Customer’s internet service provider (DSL, Fiber optic, No)
    - OnlineSecurity - Whether the customer has online security or not (Yes, No, No internet service)
    - OnlineBackup - Whether the customer has online backup or not (Yes, No, No internet service)
    - DeviceProtection - Whether the customer has device protection or not (Yes, No, No internet service)
    - TechSupport - Whether the customer has tech support or not (Yes, No, No internet service)
    - StreamingTV - Whether the customer has streaming TV or not (Yes, No, No internet service)
    - StreamingMovies - Whether the customer has streaming movies or not (Yes, No, No internet service)

3. contract and payment details:
    - Contract - The contract term of the customer (Month-to-month, One year, Two year)
    - PaperlessBilling - Whether the customer has paperless billing or not (Yes, No)
    - PaymentMethod - The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic))

4. tenure and charges details:
    - tenure - Number of months the customer has stayed with the company
    - MonthlyCharges - The amount charged to the customer monthly
    - TotalCharges - The total amount charged to the customer

5. the variable of interest:
    - Churn - Whether the customer have left the company within the last month (Yes or No)
