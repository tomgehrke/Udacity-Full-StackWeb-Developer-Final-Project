# Udacity Full Stack Web Developer Final Project

## Basic Information

* IP Address: 23.99.226.70
* Hostname: fullstack.tomgehrke.com
* SSH Port: 2200

## Configuration

### SSH

The following changes were made to the server's SSH configuration (/etc/ssh/sshd_config):

* Port 2200
* PermitRootLogin no
* PasswordAuthentication no

## Security

### User Accounts

* monkey - Student account
* grader - Mentor account (sudo access allowed)
* catalog_app (pw:mnVzG3^9) - Account for database access

### Networking

By default, the local firewall (UFW) denies incoming traffic. There are, however,
three exceptions. Access has been allowed on the following ports:

* Port 80 - HTTP
* Port 123 - NTP
* Port 2200 - for (non-standard) SSH access

### Database

A catalog_app psql role was created with the rights to create the application database.

```bash
postgres@fullstack:~$ createuser --interactive --pwprompt
Enter name of role to add: catalog_app
...
Shall the new role be a superuser? (y/n) n
Shall the new role be allowed to create databases? (y/n) y
Shall the new role be allowed to create more new roles? (y/n) n
```

### Files

The application files have been placed in `/var/www/catalog`. Rights to this folder are as follows:

```bash
drwxrwxr-x  5 root catalog_app 4096 May  9 00:53 catalog/
```

## Supporting Software

The following software has been installed:

## Third-Party Resources

* Hover (DNS)
* Azure (VM)