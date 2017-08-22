# HamsterWheel900

This is a useful python script to generate csv files to be used with RM.

## Prerequisites

* Python 2.7
* Pip
* Existing mysql database 

## How to use

* Install mysql-python
`pip install MySQL-python`
* Run the following queries in your mysql database with any TABLENAME
```create table TABLENAME (
auth CHAR(10),
username CHAR(50),
password CHAR(50),
last_timestamp TIMESTAMP
);gymdetails; 
```
* Import your existing accounts.csv files to TABLENAME and edit the last_timestamp to your liking
* Edit hamsters.py line 7-11 with your database credentials
* Run `hamsters.py` with arguments for `-dir`, `-w` and `-t` 
for example:
```
python hampsters.py -dir accounts/accounts.csv -t TABLENAME -w 4
```
will create or overwrite a file to hamsters/accounts/accounts.csv with 4 lines from the database table 'TABLENAME'