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

## **Customer Segmentation**

- **Unsupervised Learning:**
    - **KMeans**
    - **Hierarchial Clustering** (Agglomerative Clustering)
    - **DBSCAN**
    - **GaussianMixture (GMM)**
    - **Isolation Forest**

- **Optimal Clustering:**
    - **Elbow Method.**
    - **Silhouette Coefficient**.
    - **Dendogram**
    - **T-SNE**

- **Insights:**

    - **First Cluster**
        - First Cluster includes customers with high tenure.
        - First Cluster uses almost all services provided by telecom company.
        - First Cluster has a high percentage of customers that use paperless billing.
        - First Cluster includes customers with very high amount charged monthly.
        - First Cluster uses multiple lines.
        - First Cluster includes many customers with 1 and 2-year contract.
        - First Cluster use automatic and electronic check in payment more, not highly use mailed check.
    
    - **Second Cluster**
        - Second Cluster includes customers with low tenure compared to first cluster.
        - Second Cluster uses the services slightly.
        - Second Cluster has a low percentage of customers that use paperless billing.
        - Second Cluster includes customers with low or moderate amount charged monthly.
        - Second Cluster doesn't use multiple lines.
        - Second Cluster nearly doesn't include customers with 1 and 2-year contract, include more customers with month-to-month contract.
        - Second Cluster use electronic and mailed check more.
   
    - It's expected that the **Second Cluster** is the likely to **Churn** cluster and the **First Cluster** will **Not Churn**, Because:
        - First Cluster
            - high tenure.
            - charges monthly with a high amount and have multiple lines that it means they are satisfied about the provided telecom service.
            - uses all company services that it means they are very engaged and comfortable with using the system.
            - adopt the 1 and 2-year contract.
    
        - Second Cluster
            - low tenure
            - doesn't charge monthly with high amounts.
            - doesn't use the multiple lines.
            - adopt the month-to-month contracts.
