#syntax=docker/dockerfile:1.3
# Source image: ubuntu:latest
FROM ubuntu:latest

# Docker file Author
LABEL org.opencontainers.image.authors="Kryk s97650@pollub.edu.pl"

# Install required packages
RUN apt-get update &&\
    apt-get install -y apache2 &&\
    rm -rf /var/cache/apk/* 

# Copy the content of the web page
COPY ./index.html /var/www/html/

# Copy Apache2 configuration
COPY ./apache2.conf /etc/apache2/apache2.conf

# Expose the port
EXPOSE 8080

# Start Apache2 server
CMD ["apache2ctl", "-D", "FOREGROUND"]