# Server deployment for AutoClassWeb

This document explains how to deploy AutoClassWeb as a web server.


## Install Docker

Install Docker with the following [instructions](https://docs.docker.com/install/linux/docker-ce/ubuntu/).


## Install Docker Compose

Install Docker-compose with the following [instructions](https://docs.docker.com/compose/install/).


## Clone this repo
```
$ git clone https://github.com/pierrepo/autoclassweb-server.git
```

## Update configuration 

### App

Update app configuration file in `config/autoclassweb.cfg`.

If you want to receive results by e-mail, pay attention to parameters:

- `FLASK_RESULTS_BY_EMAIL`
- `FLASK_SERVER_URL`
- and all `MAIL_`


### Web server 

Update port in configuration file `docker-compose.yml`. Replace `8000` in `8000:80` with the port number where you want your server to be accessible from the Internet.


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

