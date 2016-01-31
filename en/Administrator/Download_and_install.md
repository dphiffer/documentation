---
language: English
currentMenu: install
subTitle: Download and install wallabag
---

# Download and Install Wallabag:

## I don't want to install Wallabag:

If you can't or don't want to install Wallabag on your server, we suggest you create a free account on [Framabag](https://framabag.org/) which uses our software. [Read the full documentation](../User/Framabag_account_creation.md).

## I want to install Wallabag:

### I want to download Wallabag manually:

[Download the latest Wallabag version](http://wllbg.org/latest) and unpack it:

    wget http://wllbg.org/latest
    unzip latest
    mv wallabag-version-number wallabag

Copy the files onto your web server. For Ubuntu/Debian, it is the directory /var/www/html/ :

    sudo mv wallabag /var/www/html/

Then, jump to the next section.

### I want to download Wallabag via Composer:

Install Composer:

    curl -s http://getcomposer.org/installer | php

Next, on your web server, run this command:

    composer create-project wallabag/wallabag . dev-master

Everything is downloaded into the current folder.

#### Prerequisites for your web server:

Wallabag requires that several components be installed on your web server.
To make sure your server has all the prerequisites, open the following link in your web browser:
`http://yourserver.com/wallabag/install/index.php`.

The components are:

* [PHP 5.3.3 or above](http://php.net/manual/fr/install.php) **with [PDO](http://php.net/manual/en/book.pdo.php) support**
* [XML for PHP](http://php.net/fr/xml)
* [PCRE](http://php.net/fr/pcre)
* [ZLib](http://php.net/en/zlib) (otherwise the processing of compressed pages will be affected)
* [mbstring](http://php.net/en/mbstring) and/or [iconv](http://php.net/en/iconv) (otherwise some pages will not be read - even in English)
* The [DOM/XML](http://php.net/manual/en/book.dom.php) extension
* [Data filtering](http://php.net/manual/fr/book.filter.php)
* [GD](http://php.net/manual/en/book.image.php) (otherwise pictures will not be saved)
* [Tidy for PHP](http://php.net/fr/tidy) (otherwise you may encounter problems with some pages)
* [cURL](http://php.net/fr/curl) with `Parallel URL fetching` (optional)
* [Parse ini file](http://uk.php.net/manual/en/function.parse-ini-file.php)
* [allow_url_fopen](http://www.php.net/manual/fr/filesystem.configuration.php#ini.allow-url-fopen) (optional if cURL is installed)
* [gettext](http://php.net/manual/fr/book.gettext.php) (required for multi-language support)

Install the missing components before proceeding. 

For example, to install Tidy on Ubuntu/Debian:

    sudo apt-get install php5-tidy
    sudo service apache2 reload

Note : If you're using IIS as a webserver, you have to disable *Anonymous Authentication* and [enable *Basic Authentication*](https://technet.microsoft.com/en-us/library/cc772009%28v=ws.10%29.aspx) in order to be able to login.

### Twig installation:
Wallabag is built with Twig, a template library. You have to download it for Wallabag to work.
If you cannot install `composer` (for example in the case of shared hosting), we suggest you download a file which includes `Twig`. This file can be downloaed from the page `http://yourserver.com/wallabag/index.php` (section TWIG INSTALLATION) or directly at [http://wllbg.org/vendor](http://wllbg.org/vendor). Uncompress it in your Wallabag directory.

Otherwise, you can use Composer to install `Twig` by launching `composer` from your Wallabag directory (in the case of Ubuntu/Debian: <code>/var/www/html/wallabag/</code>) by following the commands written on screen:

    curl -s http://getcomposer.org/installer | php
    php composer.phar install

### Creation of the database:

Wallabag can be installed on different types of databases:

* [SQLite](http://php.net/manual/fr/book.sqlite.php). The easiest system of all. No extra configuration needed.
* [MySQL](http://php.net/manual/fr/book.mysql.php). A well known database system which is, in most cases, more efficient than SQLite.
* [PostgreSQL](http://php.net/manual/fr/book.pgsql.php). Some people found it better than MySQL.

We advice you to use MySQL because it is more efficient. In this case, you should create a new database (for example `wallabag`),  a new user (for example  `wallabag`) and a password (here `YourPassWord`). To do this, you can use `phpMyAdmin`, or launch the following commands:

    mysql -p -u root
    mysql> CREATE DATABASE wallabag;
    mysql> GRANT ALL PRIVILEGES ON `wallabag`.* TO 'wallabag'@'localhost' IDENTIFIED BY 'YourPassWord';
    mysql> exit

*Note:* If you're using MySQL or Postgresql, you will have to **fill in all the fields**, otherwise the installation will not work and an error message will tell you what's wrong. You must create the database that you will use for Wallabag manually with a tool like PHPMyAdmin or the console.

### Permissions:

Your web server needs writing access to the `assets`, `cache` and `db` directories. Otherwise, a message will report that the installation is impossible:

    sudo chown -R www-data:www-data /var/www/html/wallabag/assets /var/www/html/wallabag/cache /var/www/html/wallabag/db

### Installation of Wallabag... At last:

Access Wallabag from your web browser: `http://yourserver.com/wallabag`. If your server is correctly configured you will reach the setup screen directly.

Select the type of database (`sqlite`, `mysql` or `postgresql`) and fill in the information about your database.
In the case of the databse MySQL created before, the standard configuration will be:

    Database engine:    MySQL
    Server:             localhost
    Database: 	        wallabag
    Username:	        wallabag
    Password:	        YourPassWord

Finally, create your first user and password (different from the database user).

Wallabag is now installed.

## Login:

From your web browser, connect to the login screen and enter your username and password.

Enjoy!
