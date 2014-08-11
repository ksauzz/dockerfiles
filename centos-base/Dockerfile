FROM centos:centos6

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN yum -y install yum-plugin-fastestmirror
RUN yum -y install wget

RUN wget http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN wget http://rpms.famillecollet.com/enterprise/remi-release-6.rpm
RUN rpm -Uvh remi-release-6*.rpm epel-release-6*.rpm

