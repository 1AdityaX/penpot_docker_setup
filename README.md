# penpot docker setup
This repo will walk you through the penpot docker setup

## Table of contents
- [What is Penpot?](https://github.com/AnonymousXsn/penpot_docker_setup#what-is-penpot)
- [Installing Penpot in a Docker Container](https://github.com/AnonymousXsn/penpot_docker_setup#installing-penpot-in-a-docker-container)
- [Logging in without actually logging in](https://github.com/AnonymousXsn/penpot_docker_setup#logging-in-without-actually-logging-in)
- [References](https://github.com/AnonymousXsn/penpot_docker_setup#references)

## What is Penpot?
Penpot is the first Open Source design and prototyping platform meant for cross-domain teams. Non dependent on operating systems, Penpot is web based and works with open standards (SVG). Penpot invites designers all over the world to fall in love with open source while getting developers excited about the design process in return.

## Installing Penpot in a Docker Container
### Install Docker
Probably the best approach to install docker is following the official docker installation guide: https://docs.docker.com/engine/install/
And the docker compose (v2). You can use the old docker-compose of course, but all the documentation supposes you are using the V2.
### Getting the docker-compose file and the config file
- [docker-compose.yaml](https://raw.githubusercontent.com/penpot/penpot/main/docker/images/docker-compose.yaml)
- [config.env](https://raw.githubusercontent.com/penpot/penpot/main/docker/images/config.env)

Create **docker-compose.yaml** and **config.env** with the contents in the above mentioned hyperlinks *(or just download them)*

### Start Penpot
```
docker compose -p penpot -f docker-compose.yaml up -d
```
This will start listening on http://localhost:9001

## Logging in without actually logging in
1. Once you have started you container, it will ask you to login.\
2. Click on the **Create an account**\
3. Once you have created an account it, will send the verfication mail.\
4. Run the below mention command in your docker shell/terminal to get the verification code
```
docker compose logs
```
5. you'll be able to find you verfication link there, open the link...and BOOM!! you have logged it!!

## References
- https://help.penpot.app/technical-guide/getting-started/#install-with-docker
- https://github.com/penpot/penpot
