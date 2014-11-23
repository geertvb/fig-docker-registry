FROM nginx

RUN \
  apt-get update && \
  apt-get -y install apache2-utils

RUN \
  htpasswd -cb /etc/nginx/docker-registry.htpasswd admin welcome1

RUN rm -f /etc/nginx/conf.d/default.conf

ADD docker-registry.conf /etc/nginx/conf.d/
