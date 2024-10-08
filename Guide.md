#  Project step-by-step execution.

## Prerequisite
1. Oracle VM Virtualbox
2. Vagrant
3. Vagrant plugins
4. Git bash or equivalent editor

**Execute below command in your computer to install hostmanager plugin**
> $ vagrant plugin install vagrant-hostmanager

## VM SETUP
1. Clone source code.
> **# git clone https://github.com/Kizhakkekkara-Vishnu-Vijayan/Clone-directory.git**
3. cd into Clone-directory.
4. cd into vagrant/Manual_provisioning

**Bring up vm's**
> $ vagrant up

**INFO: All the vm’s hostname and /etc/hosts file entries will be automatically updated. Because we have downloaded the hostmanager plugin and enbled it in the Vagrant file.**

## PROVISIONING 
### Services
```
1. Nginx => Web Service
2. Tomcat => Application Server
3. RabbitMQ => Broker/Queuing Agent
4. Memcache => DB Caching
5. ElasticSearch => Indexing/Search service
6. MySQL => SQL Database
```

### Setup should be done in below mentioned order
#### Follow the Database-conf.md setup
```
MySQL (Database SVC)
Memcache (DB Caching SVC)
```
#### Follow the Backend-conf.md setup
```
RabbitMQ (Broker/Queue SVC)
Tomcat (Application SVC)
```
#### Follow the Frontend-conf.md setup
```
Nginx (Web SVC)
```


