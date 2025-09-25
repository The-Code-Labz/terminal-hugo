---
title: Docker
date: 2025-09-24
draft: false
---
# Docker 

I have learned that docker is a great way to deploy webapp that expose itself via ports as you have complete control of the virtual enjoinment allowing a isolated box that you can do whatever you want without interfering with the global settings though once that image is made you cannot make any changes until you make a new one hence why there are so many versions with docker images but for me i have begun to rely on docker for so many of my services as I use a reverse proxy called traefik to expose all my services to port 80 and 443 so i dont have to deal with port mapping and exposing more ports than i have to it also allows me to have multiple services that use the same ports like have multiple wordpress sites but still have a way for all of them to work on the same server 

# Docker Compose

While many people like to use docker run commands `docker run nginx -d` I like having complete control and additions to my deployments 
```yaml
services:
  nginx:
   image: nginx
   container_name: nginx
   restart: unless-stopped
   networks:
     -nat 
   volumes:
     ./config:config
networks:
  nat:
   external: true 
```
---
with compose you can control so many variables in a simple yaml file then run it with the command `docker compose up -d` and that's it without trying to have all that into a docker run command 