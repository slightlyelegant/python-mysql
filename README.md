
Python MySQL Script
=======

This package contains a python script that creates a connection to a MySQL Database, reads a csv file, 
inserts the data from the CSV file, calculates a few variables from the data and then opens an HTML 
report with the calculations. 


Requirements
-------------

* Python -- one of the following:

  - Python <= 3.6
  - Pure Python MySQL Client (PyMySQL)
  - MySQL Server <= MySQL 5.7



Documentation
-------------
 1. Open config.ini file in a text editor and add your database connection configurations under the [database] section
 
 2. Open command line, navigate to script and run following

    `` ./pop_db_processor youfilenamehere.csv`` or ``python pop_db_processor YOURFILENAMEHERE.csv ``

Resources
---------

Pure Python MySQL Client (PyMySQL): https://github.com/PyMySQL/PyMySQL

MySQL Reference Manuals: http://dev.mysql.com/doc/

MySQL client/server protocol:
http://dev.mysql.com/doc/internals/en/client-server-protocol.html


License
-------

PyMySQL is released under the MIT License. See LICENSE for more information.
