FROM sk/ubuntu:18.04 AS git
LABEL maintainer="swapnil.xxxx25@gmail.com"

RUN apt-get update -y && apt-get install --fix-missing -y git

WORKDIR /opt

COPY id_rsa_github_flask_healthcheck /opt/id_rsa
ENV GIT_SSH_COMMAND='ssh -o StrictHostKeyChecking=no -i /opt/id_rsa'
RUN git clone git@github.com:swapnil-k/flask-healthcheck.git


FROM python:3.7-alpine3.10
LABEL maintainer="swapnil.xxxx25@gmail.com"

WORKDIR /opt

COPY --from=git /opt/flask-healthcheck/. /opt/
RUN pip install -r requirements.txt

ENTRYPOINT [ "python" ]
CMD [ "health_check.py" ]
