FROM php:8.0-apache
# Install the mysqli extension and enable it
RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli
# Update and upgrade the system packages
RUN apt-get update && apt-get upgrade -y
# Install git
RUN apt-get install -y git
# Clone the repository to the /var/www/html/ directory
RUN git clone https://github.com/mahmuda-bjit/Sample_Ecommerce_Project_docker.git /var/www/html/
# Replace the IP address in index.php with 'mysqldb'
RUN sed -i 's/172.20.1.101/mysqldb/g' /var/www/html/index.php
