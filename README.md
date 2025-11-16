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



STEP 6 - Group and Summerize 

----> group and summerize data by gender, income_bracket and age_group


----> Calculate Average income and average spending score 


<img width="867" height="697" alt="image" src="https://github.com/user-attachments/assets/30dec961-d6e9-47c8-abce-40d5eed3c7cb" />





STEP 7 - Export the clean data ---> cleaned_customer_data.csv




PHASE 2 - SQL Analytical Exploration 

Section A - Data Quality and Understanding 

1 - How many total customer records are in the table?
<img width="650" height="523" alt="image" src="https://github.com/user-attachments/assets/473ba8ca-384e-4713-8d98-f95434e22e49" />


2 - Are there any duplicate customer ID's? If yes, how will you handle them?


3 - How many unique genders and present, and is the distribution balanced?


4 - What is the youngest and oldest customer in the dataset?


5 - What is the average income and spending score across all cusomers? 

















