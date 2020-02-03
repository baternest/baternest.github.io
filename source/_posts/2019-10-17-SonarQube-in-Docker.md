---
title: SonarQube in Docker
date: 2019-10-17 15:16:18
categories:
tags:
---

[Get Docker Engine - Community for Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

<https://www.nico-maas.de/?p=2051>

```
# create folders for sonarqube files and postgres
sudo mkdir -p /var/sonarqube/{conf,data,logs,extensions}
sudo chown -R 999:999 /var/sonarqube
sudo mkdir -p /var/sonarqube/postgres
# make folder for all Docker files in home
mkdir ~/sonarqube
cd sonarqube
# create docker-compose.yml with following content
version: '3.1'
services:
  db:
    image: postgres:9.6-alpine
    restart: unless-stopped
    volumes:
      - /var/sonarqube/postgres:/var/lib/postgresql/data
    environment:
     - POSTGRES_USER=sonar
     - POSTGRES_PASSWORD=sonar
  sonarqube:
    image: sonarqube:6.7-community
    ports:
      - 9000:9000
      - 9092:9092
    restart: unless-stopped
    volumes:
      - /var/sonarqube/conf:/opt/sonarqube/conf
      - /var/sonarqube/data:/opt/sonarqube/data
      - /var/sonarqube/logs:/opt/sonarqube/logs
      - /var/sonarqube/extensions:/opt/sonarqube/extensions
    environment:
      - SONARQUBE_HOME=/opt/sonarqube
      - SONARQUBE_JDBC_USERNAME=sonar
      - SONARQUBE_JDBC_PASSWORD=sonar
      - SONARQUBE_JDBC_URL=jdbc:postgresql://db/sonar
# launch 
sudo docker-compose up -d

# stop
sudo docker-compose down
```

Login -> admin/admin

Webhooks -> Jenkins http://host-name/jenkins/sonarqube-webhook/

Ubuntu 16.04.6 issue

Install Docker Compose (newer version)

https://docs.docker.com/compose/install/

postgres alpine version start failed

sonarqube 7-lts
# NOTE: the default vm.max_map_count maynot be enough to 
#       run elasticsearch increase it to at least  262144
# sudo sysctl vm.max_map_count=262144

docker exec -u 0 -it container bash
