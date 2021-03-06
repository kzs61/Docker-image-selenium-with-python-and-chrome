# Selenium With Python and Chrome Driver

This repo contains Dockerfile setup to create Python Selenium environment configured to work with Chrome Driver that is used in this project: https://github.com/kzs61/petclinic-microservices-aws-docker-ansible-k8s-ci-cd


<br></br>

**Building the image and pushing to docker hub**
```
$ git clone <git-repository>
$ cd selenium-with-python-and-chrome
```
  
**Build with tag**
```  
$ docker build -t <repoName>/<imageName>:<tagName> .

example:  
$ docker build -t your_dockerhub_username/selenium-py-chrome:latest .
```

**In case you fail with some builds, you may need to clean your local storage**
```
$ docker rm -vf $(docker ps -aq)
$ docker rmi -f $(docker images -aq)
$ docker volume prune -f
```


**Login docker to push the image to docker hub**  
```
$ docker login
```
#### Pushing the image to docker hub
```
$ docker push your_dockerhub_username/selenium-py-chrome:latest
```
  
**If you receive a permission error after a pushing attempt verify your credentials for your docker hub account. 
Logout and login again (logout deletes the credentials saved during login)** 
```  
$ docker logout
$ docker login
```
