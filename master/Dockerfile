FROM drupaldocker/php:cli
MAINTAINER drupal-docker

RUN apt-get update && apt-get install -y mysql-client \
  && composer global require drush/drush:dev-master \
  && ln -s ~/.composer/vendor/bin/drush /usr/local/bin/drush \
  && drush core-status -y \
  && drush core-init -y \
  && rm -rf /var/lib/apt/lists/*

CMD ["drush", "core-cli"]
