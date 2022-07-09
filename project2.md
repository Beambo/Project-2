**PROJECT 2 DOCUMENTATION**

As usual, I had to log into our instance using AWS however i noticed that with the use of the nano instance i kept on getting a broken pipe page, research online showed it was a low memory issue which i fixed by picking a larger instance. Screenshot attached below for both error and final login page

![alt text](./Images/Error%20page.png) ![alt text](./Images/Ubuntu%20login%20page.png)

This was followed by a sudo apt update `sudo apt update` with screenshot below

![alt text](./Images/Sudo%20Apt%20Update.png)

An installation of Nginx web server was required which was done with `sudo apt install nginx` with a successful page in the screenshot below

![alt text](./Images/sudo%20apt%20install%20nginx.png)

There was a need to verify that Nginx was successfully installed and running appropirately using `sudo systemctl status nginx` with screenshot below

![alt text](./Images/System%20Status.png)

There was also the need to install MYSQL using the code `sudo apt install mysql-server` with the screenshot below as confirmation

![alt text](./Images/Sudo%20apt%20mysql%20server%20install.png)

I then needed to login to mysql to confirm the login page using the code `sudo mysql` with screenshot below

![alt text](./Images/Login%20Confirmation%20mysql.png)

I then did an interactive script by running the code `sudo mysql_secure_installation` with screenshot below

![alt text](./Images/sudo%20mysql_secure_installation.png)

I also had to install PHP with the code `sudo apt install php-fpm php-mysql` and got the screenshot below 

![alt text](./Images/PHP%20Installation.png)

I was also required to configure Nginx to make use of PHP by creating a directory, assigning ownership of the directory and then imputting the content to be echoed using the codes below and the screenshot confiming the content

1. `sudo mkdir /var/www/projectLEMP`
2. `sudo chown -R $USER:$USER /var/www/projectLEMP`
3. `sudo nano /etc/nginx/sites-available/projectLEMP`

![alt text](./Images/Project%20LEMP%20landing%20page%20code.png)

![alt text](./Images/LEMP%20landing%20page.png)

I also created a page to show additional information about our server by creating a test PHP file, getting the landing page in the screenshot below

![alt text](./Images/PHP%20landing%20page.png)

Finally, i needed to retrieve date from MYSQL database using PHP. I had to create the user to use and grant necessary permissions with the codes below and screenshot

1. `CREATE DATABASE `example_database`; `
2. `CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';`
3. `GRANT ALL ON example_database.* TO 'example_user'@'%';`

![alt text](./Images/Create%20user%20for%20use.png)

I then logged out and logged in using the new user with the new password to view the created database followed by insertion for what i want on the database using the codes `mysql -u example_user -p` `mysql> SHOW DATABASES;` `mysql> INSERT INTO example_database.todo_list (content) VALUES ("My first important item");`

The last code above allowed me to input multiple lines into my database

![alt text](./Images/Create%20Data%20Base%20and%20lines.png)

I then updated the list with a few more items by repeating the last code and got the screenshot below

![alt text](./Images/Database%20table%20completion.png)


Finally, a PHP script was created to query the database created using nano `nano /var/www/projectLEMP/todo_list.php`. The screenshot below showed a final landing page after queried.

![alt text](./Images/To%20do%20page.png)

I also added a bonus page with an addition of a line with screenshot below

![alt text](./Images/Bonus%20page%20with%20personal%20addition.png)


**THANK YOU**
