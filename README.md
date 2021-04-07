# Docker Container for uvnc repeater
Docker Container for High Performance Computing exam.

##  :pencil: Table of contents
* [Description](#description)
* [How to use](#how-to-use)
* [Setup](#setup)
* [Technologies](#technologies)
* [License](#license)


## :books: Description
In this project I created a docker container running Dott. Perri's uvnc repeater, link to the [repo](https://github.com/DamianoP/uvncrep017-ws). In RepeaterWebServer folder u can find one dockerfile for repeater container and one for web server, i used a PHP Apache Container you can find repo [here](https://github.com/geerlingguy/php-apache-container). This repeater allows you to see which servers are connected to your uvnc repeater. 
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)


## :man_technologist: How to use

## :gear: Setup
To run this project:
```
git clone https://github.com/Luchinzzz/uvncrep017-docker-container.git
cd /RepeaterWebServer
sudo docker-compose build
sudo docker-compose up -d
```

## :computer: Technologies
Project is created with:
* [Docker](https://www.docker.com/)

## :balance_scale: License 
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details

