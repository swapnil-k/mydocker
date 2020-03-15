### Why:

* Customized nginx 1.16.1 image with necessary basic packages for debug and ssh package for remote connection

#### How to build an image

* `docker build --rm -t myubuntu:16.04 ../myubuntu/.`
* `docker build --rm -t mynginx:1.16 .`

#### How to run a container

* `docker rm -f nginx`
* `docker run --name nginx --hostname nginx -p 80:80 -d mynginx:1.16`

#### Debugging
* `docker exec -it nginx bash`
* `docker logs nginx`

#### Content

* Basic ubuntu packages for general troubleshoot and debug
* Setting Indian(GMT+5:30) timezone
* Removed `sites-enabled` and `sites-available` for sake of simplicity
