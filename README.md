# Docker Store

A data store:

- push files via FTP
- serve them via HTTP

## Installation

    docker-compose build
    docker-compose up -d

## Adding FTP users

    docker-compose run ftp new-ftp-user <username>
    <enter password twice>
