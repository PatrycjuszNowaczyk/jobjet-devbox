FROM php:8.3.12-fpm

# install dependencies
RUN apt-get update && apt-get install -y \
  curl \
  git \
  zip \
  unzip \
  libpng-dev \
  libzip-dev \
  default-mysql-client

# install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Install Symfony CLI
RUN curl -sS https://get.symfony.com/cli/installer | bash && \
  mv /root/.symfony*/bin/symfony /usr/local/bin/symfony

# Create a writable directory in /tmp and symlink it to /.symfony5
RUN mkdir -p /tmp/symfony5 && \
  ln -s /tmp/symfony5 /.symfony5

# Set environment variable to point to the new writable directory
ENV SYMFONY_CLI_HOME=/tmp/symfony5

# install php extensions
RUN docker-php-ext-install pdo pdo_mysql zip gd

# Install Xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug
