# Use the official PHP image from Docker Hub
FROM php:7.4-apache

# Install PDO MySQL extension
RUN docker-php-ext-install pdo pdo_mysql

# Copy the contents of your PHP application into the container
COPY . /var/www/html/

# Set the working directory
WORKDIR /var/www/html/

# Expose port 80 to the outside world
EXPOSE 80

# Start Apache in the foreground
CMD ["apache2-foreground"]
