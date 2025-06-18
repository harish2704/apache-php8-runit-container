FROM debian:12

RUN apt-get update ;\
  apt-get install -y \
  runit-init \
  procps \
  dropbear \
  vim-tiny \
  apache2 \
  composer \
  php8.2-amqp \
  php8.2-apcu \
  php8.2-ast \
  php8.2-ds \
  php8.2-gmagick \
  php8.2-gnupg \
  php8.2-mcrypt \
  php8.2-memcache \
  php8.2-memcached \
  php8.2-mongodb \
  php8.2-msgpack \
  php8.2-oauth \
  php8.2-pcov \
  php8.2-http \
  php8.2-ps \
  php8.2-raphf \
  php8.2-redis \
  php8.2-uploadprogress \
  php8.2-uuid \
  php8.2-xmlrpc \
  php8.2-yaml \
  php8.2-zmq \
  libapache2-mod-php8.2 \
  php8.2-bcmath \
  php8.2-bz2 \
  php8.2-cli \
  php8.2-common \
  php8.2-curl \
  php8.2-dba \
  php8.2-dev \
  php8.2-enchant \
  php8.2-gd \
  php8.2-gmp \
  php8.2-imap \
  php8.2-interbase \
  php8.2-intl \
  php8.2-ldap \
  php8.2-mbstring \
  php8.2-mysql \
  php8.2-odbc \
  php8.2-opcache \
  php8.2-pgsql \
  php8.2-readline \
  php8.2-soap \
  php8.2-sqlite3 \
  php8.2-sybase \
  php8.2-tidy \
  php8.2-xml \
  php8.2-xsl \
  php8.2-zip \
  php8.2-xdebug; \
  rm -rf  /etc/sv/* ;\
  apt-get clean

RUN find /etc/init.d/ -type f  | grep -v 'apache\|dropbear\|rc' | xargs rm ;\
  find /etc/ -xtype l | xargs rm

EXPOSE 22 80 443

ENTRYPOINT ["/sbin/init", "0"]
