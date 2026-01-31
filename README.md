Project Setup
Step 1. Create a Virtual Environment
py -3 -m venv venv

Step 2: Activate the environment
venv\Scripts\activate

Step 3: Install Flask and MySQL Connector
pip install Flask flask-mysqldb

Step 4: Set Up MySQL Database
1. Open MySQL in terminal, run the following command and enter your MySQL root password when prompet-


mysql -u root -p


2. Create the Database "geeklogin" by executing the following SQL command-


CREATE DATABASE IF NOT EXISTS geeklogin DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;


3. Create the "accounts" table executing this SQL commands-


CREATE TABLE IF NOT EXISTS accounts (
    id INT(11) NOT NULL AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(255) NOT NULL,
    email VARCHAR(100) NOT NULL,
    PRIMARY KEY (id)
) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;


The query creates a database named geeklogin and switches to it using USE geeklogin;. Then, it defines a table called accounts with the following columns:

1. id – An auto-incrementing primary key to uniquely identify each user.
2. username – A unique VARCHAR(50) field to store the username (cannot be null).
3. password – A VARCHAR(255) field to store the user's password securely.
4. email – A unique VARCHAR(100) field to store the user's email (cannot be null).
5. This table is designed to manage user accounts for the login system.
