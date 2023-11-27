# Docker:  php82cake4
CakePHP 4 Application in Docker: Apache, PHP 82, mysql and phpMyAdmin in docker!
A PHP Docker application integrating Apache, PHP 82, MySQL, and phpMyAdmin offers a comprehensive environment for web development and database management within Docker containers. This setup enables a convenient and portable development environment, making it easier to deploy, manage, and scale web applications.

The key components of this Docker setup include:

CakePHP 4: CakePHP is an open-source web framework. It follows the model–view–controller approach and is written in PHP, modeled after the concepts of Ruby on Rails, and distributed under the MIT License. 

Apache:  The web server that serves the PHP web pages. It handles requests and serves the PHP content to users over the internet.

PHP 82: The scripting language used for server-side web development. It works in conjunction with Apache to process and generate dynamic web content.

MySQL: A robust and popular relational database management system. It stores and manages the application's data, providing a reliable backend for various web applications.

phpMyAdmin: A web-based graphical interface for managing MySQL databases. It simplifies tasks related to database administration, allowing users to interact with MySQL databases visually.

By encapsulating these components within Docker containers, this setup ensures portability, consistency, and ease of deployment. Developers can define and manage the entire environment via a docker-compose.yml file, simplifying setup across different machines and environments.

This Dockerized application offers an efficient workflow for web development, facilitating the creation, testing, and deployment of PHP-based web applications while also providing a user-friendly interface, via phpMyAdmin, for database management and manipulation.

# Step 1: Pull 
pull this docker from this repository 

# Step 2: go to php82cake4 folder 
cd php82cake4

# Step 3: Change env configures if you want 
open docker-compose file and cheange database user, pass, port etc if you want 

# Step 4: run compose 
dokcer-compose up -d --build 

# Step 5: install CakePHP 4
To create a project, You need to read document: https://book.cakephp.org/4/en/installation.html 
Now, go to container application directory  

 docker exec -it php82cake4 bash

It will show the directory: 
`/var/www/html`

Isside docker, check composer is installed properlly or not using following command: 
`composer -v `  

If show the version, composer is ok. 

After that, create a project using following command in the directory - composer /var/www/html:

`composer create-project --prefer-dist cakephp/app:~4.0 . `

# Step 6: enjoy 
Browse for cake application  http://localhost:8240/ 

For phpMyAdmin http://localhost:8241/

AND enjoy!
