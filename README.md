# Customer_Segmentation_Data
Customer Segmentation 

PHASE 1 - Data Cleaning and Transformation Guide 



STEP 1 - Load the data set ----> Go to home, Get data, Excel (Customer_Segmentation_Data)
Click on transform to open Power Query Editor 

STEP 2 - Confirm Data Types ----> Ensure each column has the correct data type, e.g (age -  whole number, gender - text)

STEP 3 - Create the Derived Fields ----> Create new columns, age_group and income_brcket

A) age_group column - used the 'If', 'Else' satement 

<img width="875" height="550" alt="image" src="https://github.com/user-attachments/assets/70651cda-31a9-4f7f-aa4a-32eb0d7c60e4" />

  
B) income_bracket - used the 'If', 'Else' statement 

<img width="870" height="550" alt="image" src="https://github.com/user-attachments/assets/2eb291cd-b161-4b3a-b1dd-13e02e93905c" />


STEP 4 - Add a Calculated Column ----> right click on the data fields section, click new cloumn and add formula - spend_to_income_ratio = DIVIDE([spending_score], [income], 0)


STEP 5 - Standardize text fields (capitalise gender values) 

Back to transform data ---> power query editor 

select gender column ---> right click ---> transform ---> UPPERCASE 


STEP 7 - Export the clean data ---> cleaned_customer_data.csv




PHASE 2 - SQL Analytical Exploration 

Section A - Data Quality and Understanding 

1 - How many total customer records are in the table?


<img width="596" height="447" alt="image" src="https://github.com/user-attachments/assets/c629bdfc-8c33-42f6-bcf1-f83b8b911451" />



2 - Are there any duplicate customer ID's? If yes, how will you handle them?

<img width="628" height="430" alt="image" src="https://github.com/user-attachments/assets/90636ec1-50f8-493d-a85a-c0990df5747d" />



3 - How many unique genders and present, and is the distribution balanced?

----> the distribution is not balalnced, there are more males than females. 


<img width="625" height="428" alt="image" src="https://github.com/user-attachments/assets/19b0deda-37e8-4ddb-9ed6-797e5c9bdad8" />



4 - What is the youngest and oldest customer in the dataset?

<img width="612" height="312" alt="image" src="https://github.com/user-attachments/assets/05c4a154-6bd1-416a-b0f3-c92a499b6c93" />



5 - What is the average income and spending score across all cusomers? 


<img width="552" height="393" alt="image" src="https://github.com/user-attachments/assets/d7b468ae-58c7-4198-a959-2b463ed042bb" />



SECTION B - DEMOGRAPHIC PATTERNS 

1 - What is the average age, income, and spending score for each gender?

<img width="721" height="402" alt="image" src="https://github.com/user-attachments/assets/032b959f-af51-4220-bab0-8f4278037e7e" />

2 - Which age group has the highest spending score? 

<img width="780" height="408" alt="image" src="https://github.com/user-attachments/assets/8eb3ed98-76cc-447f-a3f6-18c6ef1f529c" />

3 - How does spending behaviour vary across income_brackets (Low, Med, High)?


4 - Does higher income always lead to a hiher spending score? What patterns do you oberve? 


SECTION C - BEHAVIOURAL INSIGHTS 

1- Identify the top_spending customers (top 10 by spending_score). What's their average income and age?
<img width="641" height="630" alt="image" src="https://github.com/user-attachments/assets/0ce35c35-3c95-410a-b220-44862b4b3571" />

<img width="951" height="292" alt="image" src="https://github.com/user-attachments/assets/6ede37d4-5555-4b10-8aa7-3eebd1e746be" />

2 - Who are the low_spending customers (bottom 10 by spending_score) Explain their behaviour? 

<img width="628" height="561" alt="image" src="https://github.com/user-attachments/assets/82c81130-5d0e-411c-a84c-9e6754cb6008" />

3 - Calculate the spend_to_income_ratio for each customer?
    What range of ratios do you find (min,max,average?)
    Which customer achieved the best "value" reletaive to income?
    

4 - Which gender or age group has the highest average spend_to_income ratio?
    

    
    
























