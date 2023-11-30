FROM php:8.2-apache

# Enable Apache modules and set document root
RUN a2enmod rewrite
ENV APACHE_DOCUMENT_ROOT /var/www/html/public
RUN sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf
RUN sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf

# Install system dependencies
RUN apt-get update && apt-get install -y

# Install PHP extensions
RUN docker-php-ext-install pdo_mysql

# Set recommended PHP configurations
RUN { \
    echo 'date.timezone=UTC+7'; \
    echo 'memory_limit=-1'; \
    echo 'upload_max_filesize=100M'; \
    echo 'post_max_size=100M'; \
} > /usr/local/etc/php/conf.d/recommended.ini