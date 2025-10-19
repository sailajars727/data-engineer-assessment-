# Data Engineering Project - SQL and ETL Scripts

🧾 Project Overview

**This project has two main parts:
  A SQL script to set up the database.
  A Python ETL script to clean and load property data into the database.
  The goal is to create tables, process raw data, and load it into the target system for reporting or analysis.

**Folder Structure
  Folder	What it contains
  sql/	Database setup scripts
  scripts/	Python ETL scripts for data transformation and loading

**Requirements
  Before running the scripts, make sure you have:
  Python 3.8 or above
  Access to a database (like SQL Server, PostgreSQL, or Azure Synapse)
  Installed Python packages:
  pip install pandas pyodbc sqlalchemy

=>Step 1: Set Up the Database
    File: sql/schema.sql
  
  *What it does:
  
  This script creates the required database tables and structure for storing property data.
  
  *How to run it:
  
  Open your SQL tool (like Azure Synapse, SQL Server Management Studio, or psql).
  
  *Run the script:
  
  RUN sql/schema.sql;
  
  *Check that the tables are created:
  
  SELECT * FROM INFORMATION_SCHEMA.TABLES;

=>Step 2: Run the ETL Script
  File: scripts/etl_property_normalization.py
  
  *What it does:
  
  This script takes raw property data, cleans and normalizes it, and then loads it into your database tables.
  
  *How to run it:
  
  *Open the script and update your connection details:
  
  connection_string = "Driver={SQL Server};Server=your_server;Database=your_db;Trusted_Connection=yes;"
  
  Make sure your input data file (like a CSV) is in the right folder.

  Run the script:
  
  python scripts/etl_property_normalization.py
  
  Check your database to confirm that the data has been loaded.

  Check Results
  After the ETL process finishes:

  Verify your data in the target table:
  SELECT COUNT(*) FROM property_table;


Check the console or log messages for any errors.
