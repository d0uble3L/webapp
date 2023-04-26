
# README

This is a sample Web Application to use during Continuous Integration demos.

## Build Instruction

```text
mvn clean package

```

## Deploy instruction

Deploy ```target/WebApp.war``` on Tomcat
[here](https://github.com/d0uble3L/webapp/blob/master/Jenkinsfile#L23)

## TODO

Tools
Jenkins - Pipeline
Github - Source Code Manager
TruffleHog - Secrets Scanner (docker)
owasp/dependency-check - Software Composition Analysis (SCA)(bash script)
Sonarqube - SAST (docker container)
Maven - Build ( running on instance)
Tomcat - Web HTTP server that run java code (running on instance)
Zap - DAST (running on docker)
