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


<img width="695" height="461" alt="image" src="https://github.com/user-attachments/assets/d8bb74b8-8e34-45fa-b627-61c25f264aa7" />


2 - Which age group has the highest spending score? 


<img width="620" height="440" alt="image" src="https://github.com/user-attachments/assets/5f371ecf-1d05-4228-af14-2d4103607a61" />


3 - How does spending behaviour vary across income_brackets (Low, Med, High)?

<img width="850" height="362" alt="image" src="https://github.com/user-attachments/assets/a646080c-9e6f-4915-ae7a-214503188472" />


4 - Does higher income always lead to a hiher spending score? What patterns do you oberve? 

<img width="1003" height="403" alt="image" src="https://github.com/user-attachments/assets/690af3a2-bea5-4426-9b14-0cd236dc90b6" />


SECTION C - BEHAVIOURAL INSIGHTS 

1- Identify the top_spending customers (top 10 by spending_score). What's their average income and age?

<img width="1021" height="622" alt="image" src="https://github.com/user-attachments/assets/e75b4873-8da0-4be1-8f09-d0f8e57d9f00" />


<img width="943" height="327" alt="image" src="https://github.com/user-attachments/assets/0ec2b407-39c6-43db-8a15-cce78c7982e5" />


2 - Who are the low_spending customers (bottom 10 by spending_score) Explain their behaviour? 

<img width="665" height="552" alt="image" src="https://github.com/user-attachments/assets/c8b12bbf-0e2b-40ff-9e09-15eafd46f6c1" />

3 - Calculate the spend_to_income_ratio for each customer?
What range of ratios do you find (min, max, average?)
Which customer achieved the best 'value' relative to income?


<img width="780" height="667" alt="image" src="https://github.com/user-attachments/assets/e86e8bc3-a518-4698-afe3-685a2522dfbd" />



<img width="727" height="537" alt="image" src="https://github.com/user-attachments/assets/b093d87a-cc7e-42d4-b051-14eeab008e8b" />

 

4 - Which gender or age group has the highest average spend_to_income ratio?
    
<img width="633" height="338" alt="image" src="https://github.com/user-attachments/assets/1fde465f-2e0c-40a3-8d6c-b5a820214642" />

    

SECTION D - SEGMENT REDINESS AND MODLING PREP

1 - Group customers by age_group, income_bracket and gender - what trends emerge? 


<img width="687" height="542" alt="image" src="https://github.com/user-attachments/assets/0bbdeb8d-4b6b-45e3-902b-f2b2d656dbc9" />


2 - Which combinatons of age_group and income_bracket produce the hightest_spending_score?

3 - How many customers fall into each combination? (example, young + low income, mature + high income)

4 - Based on your findings, what featires (variables) will be most important for segmentation modeling in phase 3?   
























