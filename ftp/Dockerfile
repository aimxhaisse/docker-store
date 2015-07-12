FROM ubuntu:15.04

RUN apt-get update \
 && apt-get install -q -y vsftpd libpam-pwdfile

RUN mkdir /etc/vsftpd
ADD vsftpd.conf /etc/vsftpd.conf
ADD vsftpd.pam /etc/pam.d/vsftpd
ADD new-ftp-user /usr/bin/
RUN useradd --home /home/vsftpd --gid nogroup -m --shell /bin/false vsftpd

CMD vsftpd
