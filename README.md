# docker-compose-demo
A simple Docker Compose Demo for Spring Cloud Project .

[中文文档](http://www.liumapp.com/articles/2018/04/19/1524100110011.html) 

## how to use

* build maven project and push them into docker by running "build-images.sh"

    if you are successful , you can find this : 
    
    ![build-images.jpg](https://github.com/liumapp/docker-compose-demo/blob/master/pic/build-images.jpg)

* running project by using docker-compose :
 
        docker-compose up -d
        
    if you are successful , you can find this : 
    
    ![run-docker-compose](https://github.com/liumapp/docker-compose-demo/blob/master/pic/run-docker-compose-up.jpg)
    
    and you can find container list in your Docker pannel : 
    
    ![after-run.jpg](https://github.com/liumapp/docker-compose-demo/blob/master/pic/after-run.jpg) 
    
* stop all the project by running :

        docker-compose down          
        
* if you changed the code , plz run :

        docker-compose down 
        
        ./rm-images.sh
        
        ./build-image.sh
        
        docker-compose up
        
    the ./rm-images.sh will remove the Image from Docker : 
    
    ![rm.jpg](https://github.com/liumapp/docker-compose-demo/blob/master/pic/rm-images.jpg)
    
    the ./build-image.sh will package your project and upload it to Docker . 
    
    before you run ./build-image.sh , your Docker pannel should be look like this : 
    
    ![before-install.jpg](https://github.com/liumapp/docker-compose-demo/blob/master/pic/before-install-image.jpg)
    
    after your run ./build-image.sh  , your Docker pannel should be look like this : 
    
    ![after-install.jpg](https://github.com/liumapp/docker-compose-demo/blob/master/pic/after-install-image.jpg)
            
        
* plz pay attention , if you want to debug in IDEA , you need set your hosts file : 

        127.0.0.1 docker-compose-eureka
        127.0.0.1 docker-compose-config
        127.0.0.1 docker-compose-gateway
        127.0.0.1 demo-api-a
        127.0.0.1 demo-api-b                
        
  But jut running in Docker , you do not need set this . 
  
        