# docker-tomcat7
A docerized tomcat7

### How to use?
* Clone the code.
```
git clone https://github.com/jiasir/docker-tomcat7.git
```
* Build and Run.
```
docker build -t jiasir/tomcat7 .
docker run -d -P jiasir/tomcat7
```
* Or using Docker Hub.
```
docker run -d -P jiasir/tomcat7
```
* Using another container to update webapp and reload the process.
```
docker run -it --volumes-from="your tomcat7 container id" ubuntu:14.04 /bin/bash
docker kill --signal="HUP" "your tomcat7 container id"
```
