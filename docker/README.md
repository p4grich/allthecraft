# A tool to fetch and author Minecraft Servers to Docker.

https://minecraft.gamepedia.com/Tutorials/Setting_up_a_server

## MacOS 10.14
  * Tested on Mojave

### Software dependencies

#### Ruby:
  * Default MacOS Ruby
  * No gems required

#### Docker
  * docker

#### minecraft_deploy

A simple ruby application to list, download and author Minecraft server JAR's files to docker containers.

To list servers:
```bash
18w43c
18w43b
18w43a
1.13.2
1.13.2-pre2
1.13.2-pre1
...
$ minecraft_deploy list
``` 
To download and stage server:
Arguments -s: server version -l: licence agreement for Minecraft https://minecraft.net/en-us/realms/terms/  
```bash
$ minecraft_deploy deploy -s 1.13.2 -l true
```

To download download files:
```bash
$ minecraft_deploy download -s 1.13.2
```

To cleanup download files:
```bash
$ minecraft_deploy cleanup
```

To build and run the docker container:  
```bash
cd ~/allthecraft/docker
 
docker build -t 1.13.2 .

docker run -d -p 25565:25565 --memory="1024m" 1.13.2 
```
To run he docker container:  
```bash
cd ~/allthecraft/docker
 
docker build -t 1.13.2 .

docker run -d -p 25565:25565 --memory="1024m" 1.13.2 
```

