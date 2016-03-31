#Synopsis
The goal of the project was to to develop a Python script to parse several .csv files into tables in a relational database system. The main script in the project loops through .csv files in a directory chosen by the user  and  converts the .csv files  into sql tables within a database. You can then manage the relational database in any sql system that will handle .db files. I  used sqlite3 for my work with this script. All SQL queries written in the script are written for SQLite3

#Motivation
I served on an analysis team that needed a way to automate the processing, management and analysis of expenditure data for seven separate school districts. Each school district contained 7 years of expenditure data. Our source data provided by our client was in several messy excel files. I developed an analysis plan that could be implemented in SQL. The analysis assumed that each district was it's own database with a separate table for each year. Once this database structure was in place I can then write SQL queries to automate the rest of the analysis. The first initial challange was developing a way to convert 49 separate excel files into relations in a RDBMS. I developed this python project to tackle that issue. 

#Installation
Instructions to come.

#API Reference
Section to come

#Tests
Here is a small sample of how I have used this code. This should get you up and running pretty quickly 

from csv_to_sql import parse_sql
from csv_to_sql.NoCSVsFoundError import *
```
#Setup your path. The script will pull all .csv files from the location and convert them to tabels in the database
csv_path = r"C:\Users\brucewayne\Desktop\test\\"

#Tell the function which attributes should be treated as numeric
numeric_attr = ["StudyId", "age"]

try:
    parse_sql.to_sql(csv_path, numeric_attr, "test.db", csv_path )
except NoCSVsFoundException:
    print "No .CSV files found.\n Please check your directory or convert your files to valid .CSV format"
```
#Contributors
Written by: John Mezzanotte
If anyone has any ideas on how to improve or extend this project please let me know I would love to have some feedback. 

#License
For anyone to use on personal projects. 
