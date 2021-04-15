# Server deployment for AutoClassWeb

This document explains how to deploy AutoClassWeb on a web server.


## Install Docker

Install Docker with the following [instructions](https://docs.docker.com/install/linux/docker-ce/ubuntu/).


## Install Docker Compose

Install Docker-compose with the following [instructions](https://docs.docker.com/compose/install/).


## Clone this repo
```bash
$ git clone https://github.com/pierrepo/autoclassweb-server.git
```

## Update configuration 

### App

Update app configuration file in `config/autoclassweb.cfg`.


### Web server 

Update port in the configuration file `docker-compose.yml`. Replace `8000` in `8000:80` with the port number from which you want the AutoClassWeb service to be accessible.


## Run web serveur

From the project folder, run the following command:
```
$ docker-compose up -d
```

## Update images

First stop containers:
```
$ docker-compose down
```

Then, update images:
```
$ docker-compose pull
```

Eventually, re-run containers:
```
$ docker-compose up -d
```

