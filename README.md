# Ultimate-CICD-Pipeline
Using Jenkins to build a CI CD Pipeline as well as using docker, git, argocd, kubernetes, aws ec2 instances


1. Install Jenkins on local machine.
2. Install Docker Pipeline Plugin.
3. Install SonarQube Scanner Plugin.
4. Create New Project. Add Git for Jenkinsfile.
5. Use docker container as agent for the pipeline. Dockerfile for maven and docker in a single image.

FROM debian:bullseye-slim as build
USER root
RUN apt update && apt install -y maven \
    docker.io \
    curl \
    openjdk-17-jdk \
    && rm -rf /var/lib/apt/lists/*
WORKDIR /workspace
ENTRYPOINT ["bash"]

# Command to run the container
# docker run -it -v /var/run/docker.sock:/var/run/docker.sock shubhszone/maven-docker:v1

7. 


![image](https://github.com/user-attachments/assets/7b718575-69b6-4200-9773-ca51d6f74fca)
Sonarqube Scanner Installed
![image](https://github.com/user-attachments/assets/e30cc34a-f26a-4bb0-bd11-803ed3ff5f59)
