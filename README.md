# ansible-config
Software management configuration using ansible 

System: Red Hat Enterprise Linux Server release 7.1
Softwares: 
* Apache
* Tomcat
* Mysql 

## Enable EPEL 
```
sudo yum install wget
wget http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-5.noarch.rpm
sudo rpm -ivh epel-release-7-5.noarch.rpm
```

Add mysql in repos 
```
wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
rpm -ivh mysql-community-release-el7-5.noarch.rpm
```

Configure mysql and sepup a test db

`ansible-playbook -c local -i hosts mysql.yml` 

Configure apache 

`ansible-playbook -c local -i hosts apache.yml` 
 
