#### ubuntu

* Customized `ubuntu:18.04` image with basic packages for troubleshooting and debugging

#### How to build an image

* `docker pull ubuntu:18.04`
* `docker build --rm -t myubuntu:18.04 .`

#### How to run a container

* `docker rm -f ubuntu`
* `docker run --rm --name ubuntu --hostname ubuntu -d ubuntu:18.04`

#### Debugging

* `docker exec -it ubuntu bash`
* `docker logs ubuntu`

#### Content

* Basic ubuntu packages for general debugging
* Setting `Indian(GMT+5:30)` timezone
