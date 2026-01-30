# WordPress Deployment on Ubuntu with Nginx, PHP-FPM and MySQL

## Project Overview

This project demonstrates a complete manual deployment of WordPress on an Ubuntu Linux server using:

Nginx as the web server

PHP-FPM for PHP processing

MySQL as the database backend

---

## Objective

The objective was to understand how a production-style LEMP stack works end to end, including service configuration, permissions, SSL troubleshooting, PHP-FPM integration, and database access control.

This project was built as a hands-on infrastructure exercise suitable for DevOps, Cloud, and Linux engineering portfolios.

---

## Architecture

Client Browser
|
v
NGINX
|
v
PHP-FPM
|
v
WordPress
|
v
MySQL

---

## Technologies Used

1.Ubuntu Linux (WSL used for development)

2.Nginx

3.PHP 8.3 with PHP-FPM

4.MySQL

5.WordPress 5.6

6.Curl and OpenSSL

---

## What this Project Demonstrates

1.Manual installation of a LEMP stack

2.PHP-FPM socket configuration in Nginx

3.WordPress configuration through wp-config.php

4.Database creation and permission management

5.File ownership and permission hardening

6.SSL certificate troubleshooting in WSL environments

7.Debugging 502 Bad Gateway errors

8.PHP error tracing and log analysis

9.Web server security configuration

10.Production-style deployment process

---

## Deployment Summary

1.Install Packages

```bash
sudo apt update
sudo apt install nginx mysql-server php php-fpm php-mysql unzip curl
```

2.Create Database and User

```sql
CREATE DATABASE wordpress;
CREATE USER 'wordpress'@'localhost' IDENTIFIED BY 'wordpress123';
GRANT ALL PRIVILEGES ON wordpress.* TO 'wordpress'@'localhost';
FLUSH PRIVILEGES;
```

3.Configure NGINX to use PHP-FPM Socket

4.Download and extract Wordpress

5.Set file ownership

```bash
sudo chown -R www-data:www-data /var/www/html
```

6.Configure wp-config.php with database credentials.

7.Restart services and verify installation.
