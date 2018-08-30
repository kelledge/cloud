FROM jenkins/jenkins:lts
USER root

ENV AWS_DEFAULT_REGION us-east-1

RUN apt-get update && \
    apt-get install -y \
        apt-transport-https \
        ca-certificates \
        curl \
        wget \
        jq \
        python-pip && \
    apt-key adv --keyserver keyserver.ubuntu.com --recv 8D81803C0EBFCD88 && \
    echo 'deb [arch=amd64] https://download.docker.com/linux/ubuntu xenial stable' > /etc/apt/sources.list.d/docker.list && \
    apt-get update && \
    apt-get install -y docker-ce && \
    pip install \
        awscli \
        docker-compose
