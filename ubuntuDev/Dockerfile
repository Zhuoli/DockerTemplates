ARG  CODE_VERSION=latest
FROM ubuntu:${CODE_VERSION}
MAINTAINER zhuoli (zhuoliseattle@gmail.com)

RUN echo 'APT::Install-Recommends 0;' >> /etc/apt/apt.conf.d/01norecommends \
 && echo 'APT::Install-Suggests 0;' >> /etc/apt/apt.conf.d/01norecommends \
 && apt-get update \
 && apt-get install -y sudo openssh-server 

RUN apt-get install -y g++ gdb gdbserver

CMD service ssh start > out.log

