# Customer_Segmentation_Data
Customer Segmentation 

Phase 1 - Data Cleaning and Transformation Guide 

Step 1 - Load the data set ----> Go to home, Get data, Excel (Customer_Segmentation_Data)
Click on transform to open Power Query Editor 

Step 2 - Confirm Data Types ----> Ensure each column has the correct data type, e.g (age -  whole number, gender - text)

Step 3 - Create the Derived Fields ----> Create new columns, age_group and income_brcket

A) age_group column - used the 'If', 'Else' satement 


if [age] >= 18 and [age] <= 25 then "18–25"
  else if [age] >= 26 and [age] <= 35 then "26–35"
  else if [age] >= 36 and [age] <= 50 then "36–50"
  else if [age] <> null and [age] < 18 then "Under 18"
  else "51+"

<img width="875" height="550" alt="image" src="https://github.com/user-attachments/assets/70651cda-31a9-4f7f-aa4a-32eb0d7c60e4" />

  

B) income_bracket - used the 'If', 'Else' statement 


if [income] < 40000 then"Low"
else if [income] >= 40000 and [income] <=80000 then "Mid"
else "high"



