# Spring Ninja Box
base vagrant box for environment production with spring boot 


#Warning 
    box in development

#Contains

* Nginx
* Spring Boot
* MySQL (*TODO*)


#Requirements
  
  * VirtualBox
  * Vagrant
  * Ansible


#Sample

    spring boot application within the repository as an example : ninja-box-0.0.1-SNAPSHOT.jar
    
#Proposal

    To prepare your application production environment you only have 
    to run the *mvn clean package* command of your project,
    put into the vagrant directory and run vagrant up .

    Obviously also change the DNS in nginx.conf
    
#Execute

    clone the repository and run the command vagrant up
    and access the IP 192.168.33.21 in your broswer that will be 
    running the sample application


