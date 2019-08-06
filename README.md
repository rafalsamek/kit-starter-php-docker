 # kit-starter-php-docker
 PHP on Docker starter application

## Create docker-machine instance in Linux:
1. cd to root directory of the project but different from /home as linux uses it e.g /home/current_user
```
cd /home/rafal
```
2. Export VIRTUALBOX_SHARE_FOLDER
```
export VIRTUALBOX_SHARE_FOLDER="$PWD:$PWD"
```
3. Create docker-machine
```
docker-machine create -d virtualbox kit-starter-php-docker
```
4.
```
eval "$(docker-machine env kit-starter-php-docker)"
```

## Create docker-machine instance in Windows:
1. Create docker-machine using specifig boot2docker.iso
```
docker-machine create -d virtualbox --virtualbox-boot2docker-url https://github.com/boot2docker/boot2docker/releases/download/v18.09.8/boot2docker.iso kit-starter-php-docker
```
2.
```
eval "$(docker-machine env kit-starter-php-docker)"
```

 ## Start service in CLI:
 ```
docker-machine start kit-starter-php-docker
docker-compose -f /home/rafal/PhpstormProjects/kit-starter-php-docker/docker-compose.yml up -d --build
```
 
 ## Check the docker-machine IP and run the project in Browser:
 ```
 docker-machine ls
 ```
 
