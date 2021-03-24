FROM ubuntu:16.04
MAINTAINER Phusion <info@phusion.nl>

COPY . /bd_build

RUN /bd_build/prepare.sh 
RUN	/bd_build/system_services.sh 
RUN	/bd_build/utilities.sh 
RUN [ "/usr/bin/apt", "install", "-y",  "runit" ]
RUN	/bd_build/cleanup.sh

ENV DEBIAN_FRONTEND="teletype" \
    LANG="en_US.UTF-8" \
    LANGUAGE="en_US:en" \
    LC_ALL="en_US.UTF-8"

CMD ["/sbin/my_init"]
