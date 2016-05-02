# Linux-Server-Configuration

Udacity Full Stack Nanodegree project 5

---------------------------------------

## Objective

Take a baseline installation of a Linux distribution on a virtual machine and prepare it to host a web applications, to include installing updates, securing it from a number of attack vectors and installing/configuring web and database servers.


## Server Details

Server IP address: 52.37.82.202

SSH port: 2200

Application URL: http://ec2-52-37-82-202.us-west-2.compute.amazonaws.com/


## Configuration notes
The following changes were made to the server:  
- Create a new user named grader and give the permission to sudo
- Update all currently installed packages  
- Change the SSH port from 22 to 2200  
- Configure the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123)  
- Install and configure Apache to serve a Python mod_wsgi application  
- Install and configure PostgreSQL (to not allow remote connections)
- Create a new user named catalog that has limited permissions (and also disable default postgres user)
- Install git, clone and setup the Catalog App project from [Project 3](https://github.com/unjo63/catalog) (required updating google and facebook oauth settings, and configuring static file uploads)
- Install python-pip, python-psycopg2 and the following python libraries (requests, oauth2client, sqlalchemy, flask)
- Setup /etc/hostname and /etc/hosts

## Resources used  
Server settings:  
https://help.ubuntu.com/community/Sudoers  
http://askubuntu.com/questions/115151/how-to-setup-passwordless-ssh-access-for-root-user  
https://help.ubuntu.com/community/UFW  

Apache/mod_wsgi  
https://www.digitalocean.com/community/tutorials/how-to-configure-the-apache-web-server-on-an-ubuntu-or-debian-vps
http://flask.pocoo.org/docs/0.10/deploying/mod_wsgi/  

Postgresql:  
http://www.postgresql.org/docs/9.3/static/auth-pg-hba-conf.html
http://askubuntu.com/questions/256534/how-do-i-find-the-path-to-pg-hba-conf-from-the-shell  
http://www.techonthenet.com/postgresql/grant_revoke.php  
http://www.postgresql.org/docs/8.2/static/sql-alterrole.html  

Google/Facebook:  
https://console.developers.google.com/home/dashboard  
https://developers.facebook.com/apps  


