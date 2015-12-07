# StorageModule

##Introduction

The StorageModule is used to store files and related information. 

This module has the MySQL and you can find one database called laravel, which includes the all the tables we use to store information. When people use the Add API to add new files, the related information like file name, file address, will add into the database in this module.

This module achieves the goal that we can index the information from different remote machines and different databases not only from the local machine.

##Deployment Steps
We use Vagrant to deploy the development environment.

###Download and install vagrant
Vagrant download link: https://www.vagrantup.com/downloads.html

###Init a Ubuntu 14.04 virtual machine with the required develop envrionment

#####We have upload a vagrant box wiht required development envrionment in https://atlas.hashicorp.com/FTS, please download the version 2.0 one

if you want to modify the virtual machine:
```
$ vagrant ssh
```

##Run the module

remember to modify the file name to StorageModule
```
$cd StorageModule
```
```
$vagrant up
```

