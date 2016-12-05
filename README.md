# Docker-Sinatra-Postgresql
Automatic provisioning with Docker, a web application using sinatra framework and postgres 9.6 database

This code will allow to any developer to deploy automatically a virtual infrastructure containing:

* One web application server with Sinatra framework
* One database using postgresql

This kind of infrastructure was deployed under a Linux based operating system, specifically ubuntu 14.04.

### Required Software:
* Docker
* Docker-Compose

In the sections below, instructions for executing the provisioning infrastructure are presented:

### Clone the repository
Clone the repository to any folder in your computer
```sh
git clone https://github.com/andresort28/docker-sinatra-postgres.git 
```

### Download Cocker images
Just pull 2 docker images from docker hub. Open a terminal a type the following:
```sh
docker pull centos:7
docker pull postgres
```

### Deploy
Open a terminal, go to the directory where you cloned the repository, and deploy in this way:
```sh
docker-compose build
docker-compose up
```

### Verify
Open a browser and type http://172.17.0.1 to see the website. Type "/devices" or "/brands" to view the queries to the database according to the web server. If it does not work, just type http://localhost

## Contract RESTful

Theses are the web services offered for the web application

|   Method       | Description    |
| :------------- | :------------- |
| GET  {{host}}/ | Get a testing message of RESTful       |
| GET  {{host}}/devices | Get the name of all the devices in the database       |
| GET  {{host}}/brands | Get the name of all the devicellphones brands in the database       |


### Stop
When you want to stop the docker containers, just open again the terminal, go to the directory where you cloned the repository and press CTRL+C to stop the process, and then type:
```sh
docker-compose down
```

Ready !

## Contribute
Github is all about contributions. If you think you can collaborate or improve this, please make sure you send me a pull request

## License
Copyright (c) 2016 [Andres Ortiz](http://www.andresfelipeortiz.com).  
Licensed under the MIT license.