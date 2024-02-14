# BobApp

## Sonar Cloud
Front-end  
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=codebygaetan_BobApp_front&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=codebygaetan_BobApp_front)

Back-end  
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=codebygaetan_BobApp_back&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=codebygaetan_BobApp_back)

## Docker Hub
Front-end  
[![DockerHub Front](https://img.shields.io/badge/dockerhub-bobappfront-blue.svg?logo=Docker)](https://hub.docker.com/repository/docker/codebygaetan/bobapp-front/general)

Back-end  
[![DockerHub Front](https://img.shields.io/badge/dockerhub-bobappback-blue.svg?logo=Docker)](https://hub.docker.com/repository/docker/codebygaetan/bobapp-back/general)

## Clone project

> git clone XXXXX

## Front-end

Go inside folder the front folder:

> cd front

Install dependencies:

> npm install

Launch Front-end:

> npm run start;

## Back-end

Go inside folder the back folder:

> cd back

Install dependencies:

> mvn clean install

Launch Back-end:

>  mvn spring-boot:run

Launch the tests:

> mvn clean install


## Docker Deployment

Create a network for the app :

> docker network create bobapp_ntwk

### Back-end

Go inside folder the back folder:

> cd back

Build the Back-end container:

> docker build -t bobapp-back .

Start the container:

> docker run --network bobapp_ntwk -p 8080:8080 --name bobapp-back -d bobapp-back

### Front-end

Go inside folder the front folder:

> cd front

Build the container:

> docker build -t bobapp-front .

Start the container:

> docker run --network bobapp_ntwk -p 4200:80 --name bobapp-front -d bobapp-front