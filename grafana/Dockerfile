FROM ksauzz/base

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN apt-get update
RUN apt-get install --no-install-recommends -y wget nginx
RUN apt-get clean

RUN wget http://grafanarel.s3.amazonaws.com/grafana-1.6.0.tar.gz
RUN mkdir -p /var/www
RUN tar zxfv grafana-1.6.0.tar.gz
RUN mv grafana-1.6.0 /var/www/grafana
ADD config.js /var/www/grafana/
RUN chown -R www-data:www-data /var/www/

RUN sed -i '1s/^/daemon off;\n/' /etc/nginx/nginx.conf

RUN mkdir -p /etc/nginx/sites-enabled
ADD nginx.conf /etc/nginx/sites-enabled/default

EXPOSE 8080

CMD nginx
