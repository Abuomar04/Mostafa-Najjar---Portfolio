FROM php:8.2-apache

WORKDIR /var/www/html
COPY . /var/www/html

# make Apache look for index.php
RUN printf "<IfModule mod_dir.c>\nDirectoryIndex index.php index.html\n</IfModule>\n" \
    > /etc/apache2/conf-available/dirindex.conf && a2enconf dirindex

EXPOSE 80
CMD ["apache2-foreground"]
