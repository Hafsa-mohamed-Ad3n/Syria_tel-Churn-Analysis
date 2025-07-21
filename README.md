# Syria_tel-Churn-Analysis

![Customer Churn Illustration](Images/Customer-Churn.webp)

## Business Understading
Customer churn occurs when a customer cancels their services or switches to another provider. For Syriatel, this represents a serious threat to profitability and long-term sustainability. In the highly competitive telecommunications industry, where churn rates typically range from 15% to 25%,  churn is one of the most critical performance metrics to monitor and reduce.

Retaining customers is a central part of Syriatel’s strategy. This is because it is significantly more cost-effective to keep existing customers than to acquire new ones. Research shows that acquiring a new customer can be 5 to 10 times more expensive than retaining an existing one. 

Syriatel is one of Syria’s leading telecommunications providers, offering mobile and data services to millions of customers across the country. However, due to the competitive nature of the industry, retaining customers is increasingly challenging. To maintain its market position and continue delivering high-quality services, Syriatel must find effective ways to understand and reduce customer churn.

The objective of this project is to analyze customer behavior and predict churn using machine learning techniques. By identifying customers at high risk of churning, Syriatel can apply targeted retention strategies to improve customer satisfaction and loyalty. 

### Stakeholder

- The key stakeholders for this project include:  
   - Syriatel Management : To strategize & Implement Customer retention programs
   - Marketing Team: Interested in identifying at-risk customers for targeted retention campaigns.
   - Customer Service Team: They need to understand how support quality and call volume relate to churn so that they can help.
   - Finace Team: Monitors revenue impact from Customer loss and use this insights to forecast revenue and allocate budgets to retention.


### Objectives

- This project aims to:

   - Classify customers as likely to churn ("True") or stay ("False").
   -  Identify factors that contribute most to customer churn.
   - Enable actionable insights to guide SyriaTel’s marketing, sales, and support teams in preventing churn.



## Data Understanding

### Data source

The dataset used for this project is from Kaggle: [Churn in Telecoms Dataset](https://www.kaggle.com/datasets/becksddf/churn-in-telecoms-dataset)


### Variabe Description

- The dataset provided contains customer-level usage and service information from SyriaTel, aimed at identifying patterns that lead to customer churn. 
- The dataset has 3333 rows which represents customers and 21 column which captures features that influence their decision to stay (Not churned) or leave(Churned) the service.
- There are 20 features (independent variables) and 1 target variable (churn). Below is a breakdown of each variable:
   1. state - This shows the state where the customer resides and it can be help identify geographic patterns in churn.
   2. area code - Associated with the customers Phone number.
   3. phone number - Customer's phone number (serves as an Unique identifier)
   4. account length- Duration of customer’s relationship with SyriaTel. 
   5. international plan- Indicates whether the customer has an international calling plan (`yes`/`no`)
   6. voice mail plan - Indicates whether the customer has subscribed to voice mail service plan (`yes`/`no`)
   7. total day calls - Total number of calls made during the day
   8. total day minutes - Total number of minutes the customer has spent on calls during the day
   9. total eve minutes - Total minutes of calls made in the evening
   10. total eve calls - Total number of evening calls
   11. total night minutes- The total number of minutes the customer has spent on calls during the night.
   12. total night calls - The total number of calls the customer has made during the night
   13. total intl minutes -  The total number of minutes the customer has spent on international calls.
   14. total intl calls  -  The total number of international calls the customer has made.
   15. number vmail messages - Number of voice mail messages the customer has received.
   16. total night charge - The total charges incurred by the customer for nighttime calls.
   17. total intl charge - The total charges incurred by the customer for international calls.
   18. total eve charge - Total charges Incurred by the customer for evening call
   19. total day charge - Total charge incurred by the customer for daytime calls
   20. customer service calls - The number of times the customer has called customer service.
   21. churn -  Whether the customer has churned (`True` = churned, `False` = active)

 ### Data Limitation:
- Class Imbalance: about 85.5% of the customers did not churn, while only 14.5% did. This imbalance can affect model performance by making it biased toward predicting the majority class.

### Data Preparation:
- This involves preparing the dataset for analysis and modeling. I carried out the following:

   - Reviewed the structure of the dataset and summarized key statistics
   - Checked for missing values
   - Removed irrelevant columns, such as phone numbers, that don't add value to the analysis
   - Verified and corrected data types where necessary
   - Identified and removed duplicate records where applicable
   - Detected outliers
   - Encoding Categorical Features
   - Data Normalization

 ####  Feature types
 - Categorical Variable:
   - state
   - area code
   - international plan
   - voicemail plan

- Numerical Variable: 
   - account length
   - number vmail messages
   - total day minutes
   - total day calls
   - total day charge
   - total eve minutes
   - total eve calls
   - total eve charge
   - total night minutes
   - total night calls
   - total night charge
   - total intl minutes
   - total intl charge
   - customer service calls  

 ## Exploratory Data Analysis (EDA) 
- Churn Rate
- Distributions of Numeric & Categorical features
- Factors that contribute most to customer churn.
- Univariate Analysis
- Bivariate Analysis

### Churn Distribution
- From the class distribution, we observe that 85.5% of the customers did not churn while only 14.5% churned. This shows a significant class imbalance. 

![Churn Distribution](Images/Churn%20Distribution.png)

### Distribution of Numerical & Categorical Variable
<p float="left">
  <img src="Images/Churn_Distribution.png" width="45%" />
  <img src="Images/Churn_Distribution.png" width="45%" />
</p>

<p align="center">
  <img src="Images/Churn_Distribution.png" width="45%" />
  <img src="Images/Churn_Distribution.png" width="45%" />
</p>

