FROM php:5.6-fpm

RUN apt-get update && apt-get install -y \
		libfreetype6-dev \
		libjpeg62-turbo-dev \
		#libmcrypt-dev \
		#libpng12-dev \
		curl \
		git \
		nano \
		#libmysqlclient-dev \
		#php5-redis \
		redis-server \
	&& docker-php-ext-install pdo pdo_mysql zip \
	&& docker-php-ext-install -j$(nproc) iconv mcrypt \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install -j$(nproc) gd \
	&& curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

#RUN composer update ext-redis