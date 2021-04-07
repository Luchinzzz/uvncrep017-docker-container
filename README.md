# Docker Container for uvnc repeater
Docker Container for High Performance Computing exam.

##  :pencil: Table of contents
* [Description](#description)
* [How to use](#how-to-use)
* [Setup](#setup)
* [Technologies](#technologies)
* [License](#license)


## :books: Description <a name="description"/>
In this project I created a docker container running Dott. Perri's uvnc repeater, link to the [repo](https://github.com/DamianoP/uvncrep017-ws). In RepeaterWebServer folder u can find one dockerfile for repeater container and one for web server, i used a PHP Apache Container you can find repo [here](https://github.com/geerlingguy/php-apache-container). This repeater allows you to see which servers are connected to your uvnc repeater. In this image below you can see an example of uvnc repeater's running:
![alt text](https://github.com/Luchinzzz/uvncrep017-docker-container/blob/main/example.jpeg) <a name="image"/>

## :man_technologist: How to use <a name="how-to-use"/>
In RepeaterWebServer folder you can find folders for containers, one for uvnc repeater and one for web server, and docker compose file. In both subfolders there are dockerfile to build the containers and other file needed to run repeater, for more info see this [page](https://github.com/DamianoP/uvncrep017-ws). The app directory is needed to share datas between repeater and webpage. 
After the [installation](#setup), you can see web page like [this](#image) in any browser just going on link ``` localhost/index.php```.
You can customize some alias for the servers in the uvncrepeater.ini
Generally in the uvncrepeater.ini, servers are indicated with this kind of structure:
```
idlistN=serverID;
```
If you want, you can add an alias as server name after the ;
The alias will be used inside the WebPage.
For example:
```
idlist0=12345;gamingPC
idlist1=12346;Alex
idlist1=12347;kitchenPC
```
## :gear: Setup <a name="setup"/>
To run this project you need to install first both [Docker Engine](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/). Then you just need to type in a shell:
```
git clone https://github.com/Luchinzzz/uvncrep017-docker-container.git
cd /RepeaterWebServer
sudo docker-compose build
sudo docker-compose up -d
```
## :computer: Technologies <a name="technologies"/>
Project is created with:
* [Docker](https://www.docker.com/)

## :balance_scale: License  <a name="license"/>
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details

