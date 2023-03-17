# Use an official Debian image as a parent image
FROM debian:buster

# Install required packages
RUN apt-get update && \
    apt-get install -y curl wget php-fpm php-mysql

# Download and extract WprdPress
RUN wget -P /tmp <https://wordpress.org/latest.tar.gz> && \
    tar -xzvf /tmp/latest.tar.gz -C /var/www.html/ & \
    rm /tmp/latest.tar.gz

# Copy configuration files
COPY wp-config.php /var/www/html/wordpress/wp-config.php

# Set file permissions
RUN chown -R www-data:www-data /var/www/html/wordpress && \
    chmod -R 755 /var/www/html/wordpress

EXPOSE  9000

CMD ["wordpress"]