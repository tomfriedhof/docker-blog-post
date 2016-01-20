FROM jenkins:1.625.2

USER root

# Add the new gpg key
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

# Add the repository
RUN echo "deb http://apt.dockerproject.org/repo debian-jessie main" > /etc/apt/sources.list.d/docker.list

VOLUME /var/lib/docker

RUN apt-get update && \
  apt-get -y install \
    docker-engine 


