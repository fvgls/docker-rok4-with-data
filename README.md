# docker-rok4-with-data

Docker composition configuration to deploy Nginx, Rok4 and two data pyramids

## Description

This repository contains :
* A docker-compose configuration
* A Nginx configuration

The docker-compose configuration contains :
* A Nginx server (docker image [nginx](https://hub.docker.com/_/nginx/) )
* A Rok4 server (docker image [dolite/rok4](https://hub.docker.com/r/dolite/rok4/) )
* 2 data pyramids (docker images [dolite/data-scan1000](https://hub.docker.com/r/dolite/data-scan1000/) and [dolite/data-bdortho-d075](https://hub.docker.com/r/dolite/data-bdortho-d075/) )

The Nginx configuration redirect requests on port 80, path /rok4 to rok4, port 9000

## Requirements

Have an host with docker engine and docker-compose installed, a working connection

## Use

To run the application, in the main directory :
docker-compose up

### Change the listening port

To change the listening port on the host (1234 by default), change the line in the file `docker-compose.yml` :

    nginx:
    image: nginx
    ports:
      - "1234:80" <----------------

