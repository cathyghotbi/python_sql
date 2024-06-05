# python_mysql
In this repository, a simple database application is created using python and mysql.

* cookbook for database application with python:

* How to Install Ubuntu 20.04 LTS on VirtualBox in Windows 10
https://www.youtube.com/watch?v=x5MhydijWmc

* Beginner's Guide: Installing Python 3 on Ubuntu | Step-by-Step Tutorial
https://www.youtube.com/watch?v=IqETj6wHkfs

ubuntu terminal (cathy@test: ~$):
python3 --version
sudo apt update
suod apt install python3
pip3 --version
sudo apt install python3-pip

* IDE 
How to install PyCharm on Ubuntu 20.04 LTS / Ubuntu 22.4 LTS (Linux)
https://www.youtube.com/watch?v=15daSz2QExo

* download pycharm from https://www.jetbrains.com/
snap find pycharm
sudo snap install pycharm-community --classic

* start pyharm, add new project, new py file and just start your code there

* python in database applications
https://www.w3schools.com/python/python_mysql_getstarted.asp
https://dev.mysql.com/doc/

* install mysql ubuntu
https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04

sudo apt update
sudo apt install mysql-server

// ensure server is running
sudo systemctl start mysql.service

// avoid error requiring password
sudo mysql // open up mysql prompt
mysql > alter user 'root'@'localhost' identified with mysql_native_password by 'password';
mysql > exit

sudo mysql -u root -p 
password

// no need to enter pass to use db
mysql > alter user 'root'@'localhost' identified with auth_socket;

click on red lamp of error in python on 
import mysql.connector > it will install needed thing :)

with root user database is not accesible from mysql code in python, so a user is added and privileges granted
cathy@test: ~$ sudo mysql
mysql> creare user 'cathy'@'localhost' identified with mysql_native_password by 'password';
mysql> alter user 'cathy'@'localhost' identified with mysql_native_password by 'password';
mysql > grant all privileges on *.* to 'cathy'@'localhost' with grant option;
mysql > flush privileges; 
mysql > exit


for copy-pasting between ubuntu and windows:
download.virtualbox.org/virtualbox > choose a version > VBGuestAdditions
https://help.ubuntu.com/community/VirtualBox/GuestAdditions
sudo apt-get install virtualbox-guest-additions-iso
cd /cdrom/
cd /media/cathy/
sudo sh ./VBox_GAs_7.0.18 // the downloaded version

open folder and use shared folder between ubuntu and windows
