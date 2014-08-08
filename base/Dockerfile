FROM ubuntu:12.04

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN echo deb http://jp.archive.ubuntu.com/ubuntu/ precise main universe | tee /etc/apt/sources.list
RUN echo deb http://jp.archive.ubuntu.com/ubuntu/ precise-security main universe | tee -a /etc/apt/sources.list
RUN echo deb http://jp.archive.ubuntu.com/ubuntu/ precise-updates main universe | tee -a /etc/apt/sources.list
RUN apt-get update
