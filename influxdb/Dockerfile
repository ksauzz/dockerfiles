FROM ksauzz/base

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN apt-get install --no-install-recommends -y wget
RUN wget http://s3.amazonaws.com/influxdb/influxdb_0.7.3_amd64.deb
RUN dpkg -i influxdb_0.7.3_amd64.deb

ADD config.toml /opt/influxdb/shared/config.toml

EXPOSE 8083 8086 8090 2003

CMD influxdb -config /opt/influxdb/shared/config.toml
