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

There are no records of customer ID's in this dataset. 

3 - How many unique genders and present, and is the distribution balanced?

----> the distribution is not balalnce as there are more males than females. 

<img width="572" height="426" alt="image" src="https://github.com/user-attachments/assets/1136ffb1-9793-4dae-a6f8-9497fbac2812" />


4 - What is the youngest and oldest customer in the dataset?
<img width="757" height="320" alt="image" src="https://github.com/user-attachments/assets/c845971c-1a04-40a5-a5ef-a8645ab0856d" />


5 - What is the average income and spending score across all cusomers? 

<img width="627" height="381" alt="image" src="https://github.com/user-attachments/assets/8ff1a952-fe0b-4c36-a9de-61f569371b43" />


SECTION B - DEMOGRAPHIC PATTERNS 

1 - What is the average age, income, and spending score for each gender?

<img width="721" height="402" alt="image" src="https://github.com/user-attachments/assets/032b959f-af51-4220-bab0-8f4278037e7e" />

2 - Which age group has the highest spending score? 

<img width="780" height="408" alt="image" src="https://github.com/user-attachments/assets/8eb3ed98-76cc-447f-a3f6-18c6ef1f529c" />

3 - How does spending behaviour vary across income_brackets (Low, Med, High)?


4 - Does higher income always lead to a hiher spending score? What patterns do you oberve? 






















