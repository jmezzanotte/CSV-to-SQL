# CSV-to-SQL
Python script that will parse a .csv file into a table in an RDBMS
Written-by:           John Mezzanotte
Date-last-modified:   8-11-2015
Description:          Loops through .csv files in a directory and will convert tables into sql tables within a database.
                       You can then manage the relational database in any sql system that will handle .db files. 

Notes:                This program will only parse .csv files.

params:               to_sql(source_file, save_location, database_name)
                          - source_file (required)  : Full path to the directory with your .csv files
                           - save_location(optional) : Location where you want to save your database. If this is argument is omitted
                                                        the program will use the users current working directory to save the file.
                           - database_name(optional) : The name you want to use for your database. If this argument is omitted the
                                                      program will use the default name "gates_sustainability"

