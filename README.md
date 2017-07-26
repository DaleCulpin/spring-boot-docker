spring-boot-docker
=================

A simple Spring-Boot application run within a Docker container.

Supports both Maven and Gradle.


## Prerequisites

Docker CE or Docker Toolbox installed

## Building with Gradle

* ```gradle wrapper``` to generate the Gradle wrapper
* ```gradlew bootRun``` to run as SpringBoot application (not in a Docker container)
* ```gradlew build && java -jar build/libs/spring-boot-docker-0.1.0.jar``` to build the JAR file
* ```gradlew build buildDocker``` to create the Docker image


## Building with Maven

* ```mvn spring-boot:run``` to run as SpringBoot application
* ```mvn package && java -jar target/spring-boot-docker-0.1.0.jar``` to build the JAR file
* ```mvn install dockerfile:build``` to create the Docker image



## Running the application in a Docker container

* ```docker run -p 8080:8080 -t springio/spring-boot-docker```


## Using the Application

* When running as a SpringBoot application or runnable JAR visit ```localhost:8080```
* When running in a Docker container visit the port ```{docker-machine ip}```:8080, where ```docker-machine ip``` is IP address of the Docker machine running your container. This can be found by using the Docker command ```docker-machine ip```.