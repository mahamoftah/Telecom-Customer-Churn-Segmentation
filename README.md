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
        - First Cluster includes customers with **lowest tenure** (only **8%** of customers in this cluster spent (50 : 70) months with the Telecom Company).
        - First Cluster includes customers with **month-to-month contract**.
        - First Cluster use the services rarely, almost non-existent.
        - First Cluster has a high percentage of customers that use paperless billing.
        - First Cluster includes customers with low amount charged monthly.
        - First Cluster doesn't (lowest) use multiple lines.
        - First Cluster includes customers with lowest percentage of partners and dependents
        - First Cluster uses highly the fiber optic internet service.
        - First Cluster use electronic check more.
    
    - **Second Cluster**
        - Second Cluster includes customers with **moderate tenure** (**45%** of customers in this cluster spent (50 : 70) months with the Telecom Company).
        - Second Cluster include customers with **1-year contract**.
        - Second Cluster uses the services more than first cluster.
        - Second Cluster has a low percentage of customers that use paperless billing.
        - Second Cluster includes customers with moderate amount charged monthly.
        - Second Cluster uses (moderate) use multiple lines.
        - Second Cluster includes customers with more higher percentage of partners and dependents
        
    - **Third Cluster**
        - Third Cluster includes customers with **highest tenure** (**75%** of customers in this cluster spent (50 : 70) months with the Telecom Company).
        - Third Cluster includes customers with **2-year contract**.
        - Third Cluster customers use all services provided by telecom company.
        - Third Cluster has a low percentage of customers that use paperless billing.
        - Third Cluster includes customers with high amount charged monthly.
        - Third Cluster uses (highest) multiple lines.
        - Third Cluster includes a higher percentege of customers that don't use internet service compared to other clusters.
        - Third Cluster use automatic check in payment more.
        - Third Cluster includes customers with more higher percentage of partners and dependents.
   
    - It's expected that the **First Cluster** is more likely to **Churn** Because it:
        - has a low tenure.
        - doesn't charge monthly with high amounts.
        - adopts month-to-month contract.
        - charges monthly with a low amount and doesn't multiple lines that it means they are't satisfied, trusted or cared about the provided telecom service.
        - doesn't uses company services that it means they aren't engaged and comfortable with using the telecom company services or system.

- **Conclusion:**
    - I think The two clustering approaches (2 OR 3 Clusters) are valid and can be used by the business, But It's up to business if it prefers to deal with three clusters or deal with two.
    - But in my opinion, I prefered more the 3 clusters, Because I think It clearly distinguished between customers.
    - So I will adopt the second approach to provide novel insights.

- **Novel Insights (Solutions For Retention):**
  - **First Cluster: High Churn Risk**

    - **Key Characteristics:**
        - Lowest tenure, month-to-month contract, low service usage, low monthly charges, high usage of fiber optic internet, electronic check payment.
        
    - **Retention Strategies:**
        1. **Incentivize Contract Upgrade:**
          - Offer discounts or promotions to switch from month-to-month contracts to longer-term (e.g., 1-year) contracts. This could reduce churn by locking in customers for a longer period.
        2. **Usage Encouragement:**
          - Promote service packages that encourage engagement. You could offer limited-time free trials for premium services or special bundle offers.
        3. **Enhanced Customer Support:**
          - Provide dedicated customer service to assist customers in maximizing the value of their telecom services, helping to foster trust and engagement.
        4. **Rewards for Tenure:**
          - Offer loyalty programs that reward customers for staying with the company longer. For example, provide discounts on monthly charges or free services after 6 or 12 months.
        
    - **Upselling Opportunities:**
        1. **Service Bundling:**
          - Upsell services they are not currently using, such as adding multiple lines, digital subscriptions, or cloud services, by offering bundle discounts.
        2. **Upgrade Internet Packages:**
          - Since they use fiber optic internet, offer higher-speed plans with attractive discounts or additional features (e.g., priority customer service).
      

    - **Second Cluster: Moderate Tenure**

        - **Key Characteristics:**
           - Moderate tenure, 1-year contract, moderate service usage, low paperless billing usage, moderate monthly charges, moderate use of multiple lines, higher percentage of partners and dependents.

        - **Retention Strategies:**
           1. **Contract Extension Offers:**
              - Incentivize contract renewals by offering benefits for moving to a 2-year contract (e.g., price locks or free upgrades).
           2. **Family Plans & Group Discounts:**
              - Leverage the higher percentage of partners and dependents by offering family plans or discounts on adding more lines.
           3. **Paperless Billing Adoption:**
              - Encourage paperless billing by offering a small monthly discount for switching to this option, improving customer satisfaction while reducing operational costs.
        
        - **Upselling Opportunities:**
           1. **Service Usage Packages:**
              - Offer upselling opportunities for services they use moderately, such as data plans, entertainment bundles, or more comprehensive family packages.
           2. **Additional Lines and Features:**
              - Since they moderately use multiple lines, offer promotions for adding more lines or premium features (e.g., international calling, home security services).


    - **Third Cluster: High Loyalty**

        - **Key Characteristics:**
           - Highest tenure, 2-year contract, high service usage, low paperless billing, high monthly charges, high usage of multiple lines, higher percentage of customers without internet service, use of automatic check payment.
        
        - **Retention Strategies:**
           1. **Loyalty Programs:**
              - Reward these long-term customers with exclusive benefits, such as free upgrades, priority customer service, or discounts on premium services.
           2. **Paperless Billing Incentives:**
              - Similar to the second cluster, encourage the adoption of paperless billing through financial incentives, adding to customer convenience.
           3. **Customized Offers:**
              - Personalize offers based on their service usage to make them feel valued. For example, offer tailored packages for specific services they use most (e.g., TV bundles or home phone features).
        
        - **Upselling Opportunities:**
           1. **Cross-Sell Internet Services:**
              - Since a higher percentage of this cluster doesn't use internet services, offer attractive promotions or incentives to get them onboard with internet services.
           2. **Premium Plans:**
              - Given their willingness to pay higher amounts monthly, you can upsell premium services such as higher-tier internet speeds, enhanced security services, or entertainment packages.

    - **I think These strategies can help reduce churn in the at-risk group, increase customer satisfaction in all groups, and open up new upselling opportunities for revenue growth.**
   
## **Presentation Link**
- [Here](https://www.canva.com/design/DAGRnJjFkgo/r917vuylL5DZyEX2_cycvg/view?utm_content=DAGRnJjFkgo&utm_campaign=designshare&utm_medium=link&utm_source=editor)
