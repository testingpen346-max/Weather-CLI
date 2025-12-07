Weather App README

Username/Password for the App:
- Default Admin: username=admin, password=admin123
- Regular User: Sign up via the app or add via admin panel.

Steps to Import the Database:
1. Install XAMPP and start MySQL.
2. Open phpMyAdmin (localhost/phpmyadmin).
3. Create a database named 'weather'.
4. The app auto-creates tables on first run (via DatabaseManager.java).
5. If needed, run these SQL queries in phpMyAdmin:

   CREATE TABLE users (
id INT AUTO_INCREMENT PRIMARY KEY,
username VARCHAR(255) UNIQUE NOT NULL,
password VARCHAR(255) NOT NULL,
is_admin BOOLEAN DEFAULT FALSE,
created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
CREATE TABLE weather_history (
id INT AUTO_INCREMENT PRIMARY KEY,
city VARCHAR(255) NOT NULL,
temperature DOUBLE NOT NULL,
humidity INT NOT NULL,
description VARCHAR(255) NOT NULL,
wind_speed DOUBLE NOT NULL,
feels_like DOUBLE DEFAULT 0.0,
pressure DOUBLE DEFAULT 1013.0,
search_time DATETIME DEFAULT CURRENT_TIMESTAMP
);

Run the App:
- Compile and run Main.java in your IDE.
- Requires internet for API and MySQL running locally.

Name : Jet M Suarez
Course : 2CSB
Subject : OOP
Date : 12/7/2025

unzip using winrar or rar
