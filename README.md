<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Title of My Project
*Anton Neike*

*Data-ber-08-20, Berlin & 16/08/2020*

## Content
- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Dataset/Workflow](#dataset/workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description
The goal of this project was to import a messy data set: "Shark Attack", clean it and then export it as a CSV file. The Dataset was given to us as a CSV file.

## Dataset/Workflow
The Dataset: "Shark Atack" was a CSV file which I imported with pandas. Once I had the DataFrame, I looked at the Head to get an impression of what I had to do. Before starting to clean the data, I made a copy of the DataFrame. I then applied the following methods to clean the data:

1 - lowercase column/cell names (respect naming convention)
2 - strip(r/l) column/cell names (respect naming convention)
3 - replace whitspace with underscore in the column names (respect naming convention)
4 - check the number of null values in each column to then delete the ones with more then 3000 null values (The columns where completly empty)
5 - Check the rows where countrie has a null value to inspect the column area and location -> Fill out the countries where location or/and area gives us enough information
6 - To get a unified structure in the date column -> rename all dates which don't follow the pattern "DD-MMM-YYYY" with "not defined"
7 - Rename all years in year column that don't follow the pattern "\d\d\d\d" with not defined
8 - Deleting column: name -> because their is to much missing or false information in the colums and the use of the column is not apparent to me for any use case
9 - Deleting columns: case_number.1, case_number.2 and Href because they are duplicate
10 - In the gender column cleaning the data to have only "y", "n", Null (see code for more information)
11 - In the sex column cleaning the data to have only "m", "f", Null (see code for more information)
12 - In the age colum deleting everything which is not a number
13 - In the age colum changing the data type to a float
14 - In the age colum deleting all the age values over 120 since that is about the maximum age of the human beeing

## Organization
In the repository you will find several files:

1 - .gitignore -> To not push everything.
2 - GSAF5.csv -> The Shark Attack uncleaned CSV file
3 - GSAF5_cleaned.csv -> The cleaned Shark Attack CSV file
4 - data-wrangling.ipynb -> Contains all the code needed for importing, cleaning and exporting the file
5 - README.md -> That would be this beautiful file :P

## Links
[Repository](https://github.com/fctonio/Data-Cleaning)   