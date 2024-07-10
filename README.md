HCAHPS Patient Satisfaction Analysis:

This project analyzes patient satisfaction with hospitals in the United States using the Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) dataset. The HCAHPS dataset includes survey data from over 3,000 hospitals across the country, providing insights into various aspects of patient experience and satisfaction

Problem Statement:

In the United States, patient satisfaction is a crucial indicator of healthcare quality and is closely monitored by hospitals, policymakers, and healthcare providers. The Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) survey collects valuable feedback from patients about their hospital experiences. Despite the availability of this comprehensive dataset, understanding and improving patient satisfaction remains a complex challenge due to the multifaceted nature of healthcare services and patient expectations.

Steps Followed
1. Opening a CSV File in SQL
Load CSV Files into SQL:
Import the CSV files containing the HCAHPS survey data into your SQL database. This can typically be done using the LOAD DATA INFILE command or the import functionality of your SQL tool.
Ensure that the data is properly structured and that the column names match those in your database schema.

2. Cleaning the Data
Inspect the Data:
Examine the data for any inconsistencies, missing values, or errors.Use SQL queries to identify and address these issues.

Remove Duplicate Records:
Use SQL queries to remove any duplicate records from the dataset

Handle Missing Values:
Use SQL functions to handle or fill missing values as appropriate.


3. Joining Data from Two Files
Join the Tables:
Use SQL JOIN operations to combine data from the two CSV files based on a common column (e.g., Partiation_id, Facility_id).

Create a New Cleaned Data Table:
Save the result of the join operation into a new table for further analysis.

4. Saving the Cleaned Data into a CSV File
Export the Cleaned Data:
Use SQL export functionality to save the cleaned and combined data into a new CSV file.

5. Visualizing Data in Tableau
Open Tableau and Connect to Data
Launch Tableau:
Open the Tableau application on your computer.

Connect to CSV File:
Click on "Text File" under the "Connect" pane.
Navigate to and select the cleaned CSV file containing the data.

Data Preparation in Tableau
Review Data:
Once the CSV file is loaded, review the data in Tableau’s data source tab to ensure all fields are correctly interpreted.

Data Cleaning:
Use Tableau's data preparation tools to make any additional cleaning or transformations if required, such as renaming columns, changing data types, or creating calculated fields.

6.  Creating Visualizations

Percentage of Patient Ratings:There are tons of questions in hcahps column we are going to filter it by creaitng calculated field.
![IFIS](https://github.com/siddharam-bijjargi/Coffee-Shop-Sales-Analysis-By-Using-Excel/assets/174707306/b3af0eda-c612-4e4d-8266-3c6f701e3272)

This will show us a top Positive Answers Given by Patient.

![hcap](https://github.com/siddharam-bijjargi/Coffee-Shop-Sales-Analysis-By-Using-Excel/assets/174707306/6a67dcc9-cdf4-4af5-8944-f7f73a9db0c6)

In this we calculate the percentage of patients for each hospital rating the hospital best score.

here i am creating the calculation that's going to split out this different hospitals by small hospitals, medium hospitals, large hospitals. I am going to do based on the number of inpatient beds they have.
![12](https://github.com/siddharam-bijjargi/Coffee-Shop-Sales-Analysis-By-Using-Excel/assets/174707306/707df1b1-e561-4b29-a3f3-77379f6fa700)

but this not sufficient to filterise the data because i am getting similar hospital no. of times. Then I am creating the calculation that only select once the same hospital by using provider_ccn 
![actu](https://github.com/siddharam-bijjargi/Coffee-Shop-Sales-Analysis-By-Using-Excel/assets/174707306/5abb34eb-bd49-4805-9df7-29cc77f9c9ca) 

Question Delta from Mean Cohort:
Create a calculated field to compute the delta of survey responses from the mean of the cohort.
Drag this calculated field to the Rows shelf and visualize it using a suitable chart type, such as a bar chart.

Question Delta Spread Cohort:
Create another calculated field to measure the spread of responses.
Use box plots or scatter plots to visualize the spread across different questions.

Creating KPIs

Survey Response Rate:
Create a calculated field to compute the survey response rate.
Drag this field to the Rows shelf and visualize it using a KPI chart.

Percentage of Complete Surveys:
Create a calculated field to compute the percentage of complete surveys.
Drag this field to the Rows shelf and visualize it as another KPI.

5. Building the dashboard

Create Dashboard:
Click on the "New Dashboard" button.
Drag and drop your created visualizations onto the dashboard canvas.

Arrange Visualizations:
Arrange and resize the visualizations to create a cohesive and interactive dashboard layout.

Add Filters and Interactivity:

Add filters and interactive elements (like drop-downs or sliders) to allow users to explore the data dynamically.
