### Multi-stage build

#### First image AS git
* Install git for github repository
* SSH deploy key configuration 
* git clone

#### Second Image
* Copy source code from above image, use `--from=git`
* Simple python flask application, just a `/healthcheck` api 
* `docker build --force-rm --rm -t flask-healthcheck .`
