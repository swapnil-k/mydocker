### Openjdk:13

* Customized `openjdk 13` image with necessary basic packages for debugging

#### How to build an image

* `docker build --rm -t myubuntu:16.04 ../myubuntu/.`
* `docker build --rm -t myopenjdk:13 .`

#### How to run a container

* `docker rm -f myopenjdk`
* `docker run --rm --name myopenjdk --hostname myopenjdk -p 80:80 -d myopenjdk:13`

#### Debugging

* `docker exec -it myopenjdk bash`
* `docker logs myopenjdk`

#### Content

* Basic ubuntu packages for general troubleshoot and debug
* Setting `Indian(GMT+5:30)` timezone
* openjdk is installed in optional folder(`/opt`)
