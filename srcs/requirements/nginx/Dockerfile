FROM debian:buster

RUN apt-get clean && apt-get update && apt-get -y install nginx openssl

EXPOSE 443 8080

CMD ["nginx", "-g", "daemon off;"]