FROM ksauzz/dev-base

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN mkdir -p /usr/local/src

WORKDIR /usr/local/src
RUN wget http://download.basho.co.jp.cs-ap-e2.ycloud.jp/otp/download/otp_src_R16B03-1.tar.gz
RUN tar zxvf otp_src_R16B03-1.tar.gz

WORKDIR otp_src_R16B03-1
RUN ./configure && make && make install
