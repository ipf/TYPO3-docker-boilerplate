FROM httpd:2.4

RUN apt-get update && apt-get install -y net-tools

ADD conf/vhost.conf /usr/local/apache2/conf/.docker-vhost.conf.original
ADD ssl/*           /usr/local/apache2/ssl/
ADD entrypoint.sh   /entrypoint.sh

EXPOSE 80
EXPOSE 443
EXPOSE 8000
EXPOSE 8443

ENTRYPOINT ["/entrypoint.sh"]
CMD ["httpd"]
