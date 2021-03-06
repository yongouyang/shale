The Shale Web Framework
================

Shale is designed to be a light-weight web framework (HTTP+JSON) that is easy to use and extend. It uses 

- **Jetty** as its servlet container, 
- **Spring** to manage its beans and dependencies, 
- **Spring MVC** to provide a flexible way to create your own controller to handle request and response
- **MongoDB** as its persistent layer
- **HornetQ** as its messaging layer
- **Maven** as its build tool
- **Groovy** for writing tests
- **JUnit** as a generic testing framework
- **Mockito** as its mocking framework
- **Selenium & Cucumber** as its UI testing framework

Setup of a Deployment Environment (unix / linux)
================
1. **Create common folders**
    
        mkdir -p /app/shale/pkgs
        mkdir -p /app/shale/logs    
        mkdir -p /app/shale/tools

2. **Setup Java JDK**

    After copyping java jdk to /app/shale/tools, e.g. /app/shale/tools/jdk1.6.0_33, create a symbolic link "java" `ln -s /app/shale/tools/jdk1.6.0_33 java`
    
3. **Setup Mongo DB**

    ensure the mongodb folder has been created `mkdir -p /app/shale/storage/mongodb`
    
    download the binary `youyang@shale-dev-01:/app/shale/storage/mongodb> wget http://fastdl.mongodb.org/linux/mongodb-linux-x86_64-2.4.0.tgz`
    
    extract the compressed file to current folder `youyang@shale-dev-01:/app/shale/storage/mongodb> tar xvf mongodb-linux-x86_64-2.4.0.tgz`
    
    ensure data folders are created:
    
        youyang@shale-dev-01:/app/shale/storage/mongodb> mkdir -p /app/shale/storage/mongodb/data/db
        youyang@shale-dev-01:/app/shale/storage/mongodb> mkdir -p /app/shale/storage/mongodb/data/log
        youyang@shale-dev-01:/app/shale/storage/mongodb> mkdir -p /app/shale/storage/mongodb/data/config
    
    create a symbolic link to the mongodb binary `youyang@shale-dev-01:/app/shale/storage/mongodb> ln -s mongodb-linux-x86_64-2.4.0 mongodb-distribution`       
        
(to be updated ...)