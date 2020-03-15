#### Docker

* A bunch of dockerfiles of most common applications
* Created for `dev/qa/uat/staging` and `prod` environments

##### How to build image using Dockerfile

* `cd <app_name>`
* `docker build --rm -t <your_name>/<your_repo_name>:<tag> <path_of_Dockerfile>`
* `$(aws ecr get-login --no-include-email --region ap-south-1)`
* `aws ecr create-repository --repository-name <your_repo_name>`
* `docker push <ecr_url>/<your_repo_name>:<tag>`

##### How to run a container

* `docker run --name <container_name> --rm --hostname <hostname> -p <host_port>:<container_port> -d <yourname>/<yourreponame>:<tag>`
  
##### Debugging

* `docker exec -it <container_name>|<container_id> bash`
* `docker logs <container_name>`
* `docker inspect <container_name>|<container_id>`
