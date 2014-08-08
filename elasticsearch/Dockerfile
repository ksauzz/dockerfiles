FROM ksauzz/base

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN echo oracle-java7-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections

RUN apt-get update
RUN apt-get install --no-install-recommends -y wget python-software-properties
RUN apt-add-repository ppa:webupd8team/java
RUN apt-get update

RUN apt-get install --no-install-recommends -y oracle-java7-installer
RUN apt-get clean

RUN wget http://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-1.2.1.deb
RUN dpkg -i elasticsearch-1.2.1.deb

ADD elasticsearch.yml /etc/elasticsearch/

EXPOSE 9200

CMD /usr/share/elasticsearch/bin/elasticsearch -Des.config=/etc/elasticsearch/elasticsearch.yml
