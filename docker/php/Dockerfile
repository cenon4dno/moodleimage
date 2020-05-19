FROM php:7.2-fpm

# php-fpm

#RUN apt-get install mysqli php-xmlrpc
RUN docker-php-ext-install mysqli
RUN apt-get update
RUN apt-get install libzip-dev libpng-dev zlib1g-dev libicu-dev libxml2-dev g++ -y
RUN docker-php-ext-configure zip --with-libzip \
  && docker-php-ext-install zip



RUN docker-php-ext-install gd
#RUN docker-php-ext-configure intl
RUN docker-php-ext-install intl
RUN docker-php-ext-install xmlrpc
RUN docker-php-ext-install soap
RUN docker-php-ext-install opcache

CMD ["php-fpm"]

EXPOSE 9000
