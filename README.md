# StorageModule

In Ubuntu 14.04, we should implement apache2, php, mysql and Laravel:

###Install apache2:  
```
$ apt-get update
```  
```
$ apt-get install -y apache2
```

###Update php package to php5.6:  
```
$ sudo apt-get install python-software-properties
```   
```
$ sudo apt-add-repository ppa:ondrej/php5-5.6
```   

###Install php5.6:  
```
$ sudo apt-get update
```   
```
$ sudo apt-get install php5 php5-mcrypt
```

###Install mysql  
```
$ sudo apt-get install -y mysql-server mysql-client
```   
```
$ sudo apt-get install libapache2-mod-auth-mysql
```  
```
$ sudo apt-get install php5-mysql
```  


In order to install Laravel, we need composer:  
###Install composer  
```
$ sudo php -r "readfile('https://getcomposer.org installer')" | sudo php -- --filename=composer
```  
```
$ sudo mv composer /usr/local/bin/composer
```

###Install Laravel:  
```
$ composer global require "laravel/installer=~1.1"
```

###Set Laravel to PATH:  
````
$ cd /etc
````  
````
$ sudo nano profile
````  
````
export PATH="$PATH:/home/vagrant/.composer/vendor/bin"
````  
Now, we can use Laravel in command line.

###Let mysql allow remote connect:  
first, lonin to mysql:  

```
$ grant all PRIVILEGES on *.* to admin@'%' identified by '123456';
```

then go to mysql configuration file: 
 
```
$ cd /etc/mysql
```  
```
$ sudo nano my.cnf
```
  
then change bind address x.x.x.x to 0.0.0.0  

Now, we can access mysql remotely with user 'admin' and password '123456'.  




