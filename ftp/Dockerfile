FROM ubuntu:15.04

RUN apt-get update \
 && apt-get install -q -y vsftpd

RUN mkdir -p /srv/files/ftp
RUN usermod -d /srv/files/ftp ftp

CMD vsftpd
