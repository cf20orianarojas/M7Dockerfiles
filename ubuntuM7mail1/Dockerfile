FROM ubuntu:14.04

#FROM joaniznardo:ubuntum7base
#

MAINTAINER joaniznardo (github)

RUN apt-get update && apt-get install -y openssh-server sudo supervisor
RUN useradd -m ubuntu && echo "ubuntu:ubuntu" | chpasswd && adduser ubuntu sudo
RUN apt-get install -y postfix-cdb

CMD /etc/init.d/ssh restart && supervisord -n
