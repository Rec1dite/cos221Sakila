# COS221 Sakila Database Administraction Client

## Installation:

### Setup Sakila database:
1) Extract the `u21630276_sakila-db.zip` file in your folder of choice.
2) To load the sql dump into your MariaDB installation, navigate to the extracted folder on the command line, and execute the following commands, entering your password when prompted:

On Windows (CMD or WSL, `mysql.exe` must be available in `%PATH%`):
> mysql.exe -u root -p

On Linux:
> mysql -u root -p

3) From within the `mysql` shell, execute the following:
> source sakila-schema.sql

> source sakila-data.sql

The u21630276_sakila database should now be available in your MariaDB/MySQL shell.
To check:
> show databases;



### Setup Environment variables:
The SekilaClient application reads the following environment variables to determine how it should connect to the database:
> SAKILA_DB_PROTO
> SAKILA_DB_HOST
> SAKILA_DB_PORT
> SAKILA_DB_NAME
> SAKILA_DB_USERNAME
> SAKILA_DB_PASSWORD

Assuming that most properties should be left as default, you only need to set your `SAKILA_DB_PASSWORD` (and possibly `SAKILA_DB_USERNAME`) environment variables before running the SekilaClient app (instructions below), as the others will take on their expected default values if not manually overridden.



### This project is best viewed in the Netbeans IDE:

1) `git clone https://github.com/Rec1dite/cos221Sakila` in your folder of choice
2) From within Netbeans `Ctrl + Shift + O` to bring up the *Open Project* dialog.
3) Select **SekilaClient** in the downloaded repo folder.
4) Ensure that `<default config>` is selected in the *Set Project Configuration* dropdown menu (Usually to the left of the green triangle).
5) To compile and run, hit the green *Run Project* triangle icon, or simple hit `F6` on your keyboard.
