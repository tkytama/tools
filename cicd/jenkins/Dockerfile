FROM jenkins/jenkins:2.190.2

ENV DEBIAN_FRONTEND noninteractive

USER root

RUN apt-get update -y \
&& apt-get -y install sshpass \
&& curl -fL -o docker.tgz "https://download.docker.com/linux/static/test/x86_64/docker-19.03.4.tgz" \
&& tar --strip-components=1 -xvzf docker.tgz -C /usr/bin \
&& groupadd docker \
&& gpasswd -a jenkins docker

USER jenkins