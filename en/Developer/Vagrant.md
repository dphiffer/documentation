---
language: English
currentMenu: vagrant
subTitle: Vagrant
---

# Vagrant

In order to allow you to easily set up the required configuration for Wallabag, we offer you a Vagrant file  to be used with [Vagrant](http://www.vagrantup.com).

[According to Wikipedia,](https://en.wikipedia.org/wiki/Vagrant_%28software%29)

    Vagrant is computer software for creating and configuring virtual development environments. It can be seen as a wrapper around virtualization software such as VirtualBox, KVM, VMware and around configuration management software such as Ansible, Chef, Salt or Puppet.

## Using Vagrant for Wallabag:

Here is the procedure to run Wallabag inside a Vagrant container:

    wget -O wallabag-dev.zip https://github.com/wallabag/wallabag/archive/dev.zip
    unzip wallabag-dev.zip
    cd wallabag-dev
    vagrant up

Now, go to `http://localhost:8003`, wallabag should be available there! (make sure that port 8003 of your machine is not used for anything else).

## What Did the Vagrantfile Install?:

The script installs a LAMP server:

* Ubuntu 14.04
* an Apache2 web server
* PHP5
* SQLite or MySQL or PostgreSQL for PHP
* XDebug for PHP
