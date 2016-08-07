# DockerBoxConfig
Config files for starting my VPS.

## Setup
```sh
$ apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
$ apt-get update
$ apt-get upgrade
$ apt-get install apt-transport-https ca-certificates linux-image-extra-$(uname -r) docker-engine
$ curl -L https://github.com/docker/compose/releases/download/1.8.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
$ service docker start
$ systemctl enable docker
$ groupadd docker
$ adduser sam --group docker
$ su sam
$ cd ~
$ mkdir docker
$ cd docker
$ git clone https://github.com/StoicPerlman/DockerBoxConfig .
$ git clone https://github.com/StoicPerlman/GigMapr
$ docker build -t gigmapr:latest GigMapr/
$ docker-compose up
```
