# ⚙️ Technology Used
1. HTML5
2. CSS3
3. Core/Procedural PHP programming language
4. MySQL Relational Database

 
## 📖  How to Download the Project and Run on your PC?

### Pre-Requisites:

1. Download and Install XAMPP

[Click Here to Download](https://www.apachefriends.org/index.html)

2. Install any Text Editor (Sublime Text or Visual Studio Code or Atom or Brackets)

### Installation

1. Download as as Zip or Clone this project
2. Move this project to the afore-mentioned Directory
```
Local Disc C: -> xampp -> htdocs -> 'this project'
```
*Local Disk C is the location where xampp was installed*

3. Open XAMPP Control Panel and Start 'Apache' and 'MySQL'
     If the 'MySQL' doesnt start( it shows an error regarding an unavailable port), click the config button in the MySQL row in the control panel.
     after clicking the config button, open the my.ini text file in the dropdown. This file contains a port-number mentioned several times(3306). Change the port        number to some other number which is free/available in the netstat window.(The netstat button is available on the right in the control panel)

4. Importing Database

a. Open localhost in your browser and go to 'phpmyadmin'
b. Create a Database with the name 'clubs_iitk'  without the quotes
c. Import the SQL file provided with this project

5. Make Changes to settings

Go to 'config' folder and Open 'constants.php' file. Then make changes shown in comments below.
```php
<?php 
//Start Session
session_start();

//Create Constants to Store Non Repeating Values
define('SITEURL', 'http://localhost/CLUBS_IITK/'); //Update the home URL of the project if you have changed port number or it's live on server
define('LOCALHOST', 'localhost');
define('DB_USERNAME', 'root');        
define('DB_PASSWORD', '');                     // the password here should match the password for MySQL 
define('DB_NAME', 'clubs_iitk');
    
$conn = mysqli_connect(LOCALHOST, DB_USERNAME, DB_PASSWORD) or die(mysqli_error()); //Database Connection
$db_select = mysqli_select_db($conn, DB_NAME) or die(mysqli_error()); //SElecting Database 

?>
``` 


6. Now, Open the project in your browser using 'localhost/CLUBS_IITK'. 
    It should run perfectly.
 
