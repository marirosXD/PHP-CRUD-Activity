# PHP-CRUD-Activity

Objective of the Activity
In this activity, you will analyze and implement CRUD (Create, Read, Update, Delete) operations using PHP and PDO.

You will also apply PHP validation and user-defined functions to improve code structure and security.



Start Apache and MySQL in XAMPP

Open your browser and go to:

http://localhost/phpmyadmin
 
 
Create a database named:

pdo_transactions


STEP 1 : Database Connection (PDO)
In db.php, write the code that:
Connects PHP to MySQL using PDO
Uses try-catch
Enables error mode (ERRMODE_EXCEPTION)
This file must be included in all CRUD files.


STEP 2: Create PHP Functions
In functions.php, create at least 3 user-defined functions:

Required Functions
A function to validate numbers
Must reject negative values
A function to compute total
Price × Quantity
A function to redirect pages


STEP 3: CREATE (Insert Data)
In index.php:
Create an HTML form
Fields: Item, Price, Quantity
Use POST method
In create.php:
Receive form data
Validate price and quantity (no negative values)
Compute total using a function
Insert data using PDO prepared statements
Redirect to read.php after success




STEP 4: READ (View Records)
In read.php:
Fetch all records from the database
Display them in an HTML table
Each record must show:
Item
Price
Quantity
Total
Add:
Edit link
Delete link


STEP 5: UPDATE (Edit Record)
When clicking Edit:
Pass the record id using GET
In update.php:
Fetch the record using the ID
Display existing values in a form
On submit:
Validate inputs
Recompute total
Update the record using a prepared statement
Redirect back to read.php


STEP 6: DELETE (Remove Record)
When clicking Delete:
Pass the record id
In delete.php:
Delete the record using a prepared statement
Redirect back to read.php
Security Reminder:

Never delete using raw SQL with variables




STEP 7: Validation Rules (MANDATORY)
Your system must:

Reject negative Price
Reject negative Quantity
Validate using PHP (server-side)


STEP 8: Analysis Questions (TO SUBMIT)
Students must answer:

Explain how CREATE works from form to database
Explain how READ retrieves records
Explain why UPDATE needs an ID
Explain why prepared statements are important
Explain how functions improved your code




Source Code:

(Slight debug)



Create Database and Table
Step 2: Open phpMyAdmin
Browser → http://localhost/phpmyadmin
Step 3: Create Database
Click New
Database name:
 
pdo_transactions
 
 
Click Create
Step 4: Create Table
Table name: transactions

Field

Type

Extra

id

INT

Primary Key, Auto Increment

item

VARCHAR(100)



price

DECIMAL(10,2)



qty

INT



total

DECIMAL(10,2)



