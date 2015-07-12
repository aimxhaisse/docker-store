FROM ubuntu:15.04

RUN apt-get update \
 && apt-get install -q -y vsftpd libpam-pwdfile apache2-utils

RUN mkdir -p /etc/vsftpd /var/www /var/run/vsftpd/empty
RUN useradd --home /home/vsftpd --gid nogroup -m --shell /bin/false vsftpd

ADD vsftpd.conf /etc/vsftpd.conf
ADD vsftpd.pam /etc/pam.d/vsftpd
ADD new-ftp-user /bin/

CMD ["vsftpd"]
