FROM php:7.3-fpm

RUN pecl install xdebug-2.7.2 \
    && docker-php-ext-enable xdebug

RUN docker-php-ext-install pdo pdo_mysql

# Configure XDebug
RUN { \
      echo "xdebug.profiler_enable=0"; \
      echo "xdebug.remote_autostart=0"; \
      echo "xdebug.remote_enable=1"; \
      echo "xdebug.max_nesting_level=500"; \
      echo "xdebug.remote_host=192.168.7.133"; \
      echo "xdebug.remote_port=9000"; \
  } | tee -a /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
