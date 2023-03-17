FROM debian:buster 

# add user and group 
RUN groupadd -t mysql && userafddd -r -g mysql mysql

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get -y install mariadb-server

RUN service mysql start

EXPOSE 3306

VOLUME /var/lib/mysql

CMD ["mariadb"]