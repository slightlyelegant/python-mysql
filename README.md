Python MySQL Script
=======

This is a python script that creates a connection to a MySQL Database, reads a csv file, 
inserts the data from the CSV file, calculates a few variables from the data and then opens an HTML 
report with the calculations. 


Requirements
-------------

  - Python <= 3.6
  - Pure Python MySQL Client (PyMySQL)
  - MySQL Server <= MySQL 5.7



How to set up the script
-------------
 1. Download python-mysql.zip and extract files
 
 2. Open config.ini in a text editor and add your database connection configurations under the [database] section
 
 3. Open pop_db_processor.py in a text editor, find the following lines and add your insert and select SQL queries in between the quotes:
 
    ```
    #############################################
    
    #queries for database

    #############################################

    query_insert = '''
            YOUR_INSERT_QUERY_HERE
        '''

    query_select = '''
            YOUR_SELECT_QUERY_HERE
        '''


4. If the values in your csv files are strings, you can skipp this step -- If the values in your CSV file are not strings, you will need convert the datatypes of each value in csv row to be sure your SQL insert statement will work. Find the following
code in pop_db_processor.py and replace array with correct datatypes:

    ```
    #!!!!!important
        #convert strings from csv to integers/SQLdecimal
        rows = [[int(row[0]), int(row[1]), decimal.Decimal(row[2])] for row in reader]
        
    Sample data to match above code
    _______________________________
    
    2,3,25.7
    3,45,34.9
    234,345,456.56
    34,456,487.9



How to run the script
------------- 
 1. Open command line, navigate to directory that contains the script
 2. Run one of the following command:

    `` ./pop_db_processor youfilenamehere.csv`` or ``python pop_db_processor YOURFILENAMEHERE.csv ``

Resources
---------

Pure Python MySQL Client (PyMySQL): https://github.com/PyMySQL/PyMySQL

MySQL Reference Manuals: http://dev.mysql.com/doc/

MySQL client/server protocol:
http://dev.mysql.com/doc/internals/en/client-server-protocol.html
