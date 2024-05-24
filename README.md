# Crowdfunding_ETL
### Rafael Molina, Erika Santos, Claudia Duran


With two available datasets our group used Python and Pandas to extract and transform the data in order to create CSV files, create an ERD and upload the data into a Postgres database.

#Crowdfunding Data

##Extracting Data and create 'Category' & 'Subcategory' Dataframes
- Read excel data from resource folder and load into crowdfunding_info_df
- Split the "Category & Subcategory" column into two columns with the respective data
- Create an ID column for categories and subcategories in order to index the tables for both
- Export tables into CSVs stored into the Resource folders

##Campaign Dataframe
Make a copy of the crowdfunding dataframe and transform the new dataframe to have the following paramaters:

- The "cf_id" column
- The "contact_id" column
- The "company_name" column
- The "blurb" column, renamed to "description"
- The "goal" column, converted to the float data type
- The "pledged" column, converted to the float data type
- The "outcome" column
- The "backers_count" column
- The "country" column
- The "currency" column
- The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
- The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format
- The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
- The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

Export the dataframe as a csv and save in the Resources folder

##Contacts Dataframe
Using python iterate through the DF to convert each row into a dictionary
Split the name column into first name and last name columns then delete the name column
Reorder the columns and export the cleaned data into a CSV in the Resources folder

#ERD and Postgres
Sketch and ERD using the CSV files created
Create a table schema for each CSV file
Create a Postgres database and verify the table creation by tunning a SELECT statement for each table then import each CSV into the corresponding SQL table.
