# Telco Customer Churn Analysis

## 1. Project Overview

This project analyzes customer churn for a telecommunications company, focusing on customer behavior, revenue exposure, and retention opportunities.

The analysis aims to identify the customer segments with the highest churn risk and assess their potential financial impact, supporting data-driven retention strategies.

## 2. Business Problem

Which customer segments present the highest churn risk, and what is their potential financial impact?
Which contract types are most associated with churn?
Where should retention efforts be prioritized?

## 3. Dataset

The dataset can be obtained via the URL: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
| Column | Type | Description |
|---|---|---|
| `customerID` | Identifier | Unique customer ID. |
| `gender` | Categorical | Customer's gender (Male/Female). |
| `SeniorCitizen` | Binary | Indicates whether the customer is a senior citizen (1 = Yes, 0 = No). |
| `Partner` | Binary | Indicates whether the customer has a partner (Yes/No). |
| `Dependents` | Binary | Indicates whether the customer has dependents (e.g., children, parents) (Yes/No). |
| `tenure` | Numerical | Number of months the customer has been with the company. |
| `PhoneService` | Binary | Indicates whether the customer has phone service (Yes/No). |
| `MultipleLines` | Categorical | Indicates whether the customer has multiple telephone lines. |
| `InternetService` | Categorical | Type of internet service: DSL, Fiber optic, or No. |
| `OnlineSecurity` | Categorical | Indicates whether the customer has an online security service. |
| `OnlineBackup` | Categorical | Indicates whether the customer has an online backup service. |
| `DeviceProtection` | Categorical | Indicates whether the customer has device protection. |
| `TechSupport` | Categorical | Indicates whether the customer has technical support. |
| `StreamingTV` | Categorical | Indicates whether the customer uses a TV streaming service. |
| `StreamingMovies` | Categorical | Indicates whether the customer uses a movie streaming service. |
| `Contract` | Categorical | Contract type: Month-to-month, One year, or Two year. |
| `PaperlessBilling` | Binary | Indicates whether the customer receives paperless billing. |
| `PaymentMethod` | Categorical | Payment method used by the customer. |
| `MonthlyCharges` | Numerical | Monthly amount charged to the customer. |
| `TotalCharges` | Numerical | Total amount paid by the customer since the beginning of the contract. |
| `Churn` | Target Variable | Indicates whether the customer canceled the service (Yes/No). |

### How to use

* Download the repository.
* Open telco_customer_churn.pbix in Power BI Desktop.
* If prompted, update the Excel data source path to the local data/telco_customer_churn.xlsx file.
* Refresh the data

## 4. Methodology

### Data Preparation
* Data cleaning
* Handling categorical variables
* Adjusting decimal values to Monthly e Total Charges
* Handling Null values
* Creation of tenure groups
* Creation of monthly charge ranges

### Metrics

* Churn Metrics

| Metric                              | Description                                                                                                                                                                           
| ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Churn Rate**                      | Percentage of customers who churned relative to the total customer base.                                                                                                             |
| **Priority Segment Churn Rate**     | Churn rate of the customer segment identified as the priority for investigation and retention efforts.                                                                               |
| **Revenue at Risk**                 | Monthly revenue associated with churned customers and therefore potentially lost.                                                                                                    |
| **Active Customers**                | Number of customers who remain active in the customer base.                                                                                                                          |
| **ARPU**                            | Average monthly revenue generated per customer.                                                                                                                                      |
| **Churned ARPU**                    | Average monthly revenue generated per customer among churned customers.                                                                                                              |
| **Retained ARPU**                   | Average monthly revenue generated per customer among retained customers.                                                                                                             |
| **Churn Support Diff**              | Difference, in percentage points, between the churn rates of customers with and without Tech Support.                                                                                |
| **Customer Churn Priority Segment** | Identifies the customer segment with the highest churn risk and financial relevance for retention prioritization.                                                                    |
| **Customers Churned**               | Total number of customers who churned.                                                                                                                                               |
| **Financial Impact Index**          | Ratio between the percentage of revenue at risk and the percentage of churned customers, indicating whether the financial impact is proportionally higher or lower than the impact on the customer base. |

* Revenue & Customer Base Metrics

| Metric                                 | Description                                                                                    |
| -------------------------------------- | ---------------------------------------------------------------------------------------------- |
| **Monthly Revenue**                    | Total monthly revenue generated by the customer base.                                          |
| **Monthly Revenue at Risk**            | Monthly revenue associated with churned customers and therefore potentially lost.              |
| **Revenue at Risk – Priority Segment** | Monthly revenue at risk specifically associated with the identified priority customer segment. |
| **Total Customers**                    | Total number of customers included in the analyzed customer base.                              |
| **Total Senior Citizens**              | Total number of customers classified as senior citizens.                                       |

### Analysis

* Univariate analysis → segmentation → cross-analysis → financial impact analysis → retention prioritization.

## 5. Key Findings

01 - Overall Churn

*The overall churn rate is 26.54%, representing 1,869 customers.*



02 - Contract Type

*Month-to-month customers present the highest churn rate at 42.71%.*



03 - Internet Service

*Fiber optic customers have a churn rate of 41.89%, significantly higher than DSL customers.*



04 - Revenue Exposure

*Churned customers represent 26.54% of the customer base but account for 30.77% of monthly revenue, indicating a disproportionately higher financial impact.*



05 - Priority Segment

*The highest churn rate identified is among Month-to-month + Fiber optic + No Tech Support customers, reaching 57.52%.*



06 - Financial Exposure

*This segment represents approximately $48.2K in monthly revenue at risk.*



07 - Support Hypothesis

**Observation**: *Customers without Tech Support show substantially higher churn in the identified segment.*

**Hypothesis**: *Tech Support adoption may be associated with lower churn.*

**Next step**: *Test this relationship while controlling for tenure, monthly charges, and contract type.*

## 6. Business Recommendation

### Priority
**Prioritize Month-to-month + Fiber optic customers without Tech Support.**

### Recommended actions
* Investigate barriers to Tech Support adoption.
* Test incentives for Tech Support subscription.
* Evaluate incentives for migration to longer-term contracts.
* Monitor churn and revenue retention within the identified segment.

### Important caveat
The analysis identifies associations rather than causal relationships. Further statistical testing or experimentation would be required to determine whether Tech Support adoption directly reduces churn.

## 7. Dashboard
 * Executive Overview

Overall customer base, churn and high-level financial exposure.

<img width="1510" height="850" alt="image" src="https://github.com/user-attachments/assets/ca957214-e2fc-41f5-b7ea-26615d1645bc" />



 * Customer Churn Analysis

Identification of customer characteristics and segments associated with higher churn.

<img width="1511" height="849" alt="image" src="https://github.com/user-attachments/assets/ffbefdc8-1a92-4386-930c-cb9429738d70" />



* Revenue & Churn

Assessment of the financial impact of customer churn.

<img width="1509" height="846" alt="image" src="https://github.com/user-attachments/assets/b9b84f97-b228-47d6-82b3-ea51b2e0fcaf" />



* Retention Prioritization

Identification of the highest-risk segment and formulation of a retention hypothesis.

<img width="1512" height="847" alt="image" src="https://github.com/user-attachments/assets/b3eddc72-bf1b-4e6e-91a5-9fddf98670f6" />



## 8. Tools & Technologies

Power BI | DAX | Data Analysis | Data Visualization | Business Intelligence

## 9. Final Conclusion

The analysis indicates that customer churn is not evenly distributed across the customer base. Month-to-month contracts, Fiber optic service, and the absence of Tech Support are particularly associated with higher churn rates.

From a financial perspective, churn represents a significant exposure, accounting for 30.77% of monthly revenue despite affecting 26.54% of customers.

The analysis therefore recommends prioritizing retention efforts toward the Month-to-month + Fiber optic + No Tech Support segment, while further testing is required to determine whether Tech Support adoption has a causal effect on churn.

## Author

**Rafael Antunes**  
Data Analytics | Power BI | SQL | DAX

### AI Assistance
*I used AI tools to support English translation and documentation refinement. I developed and validated all analysis, calculations, and business conclusions myself*
