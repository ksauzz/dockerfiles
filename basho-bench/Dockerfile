FROM ksauzz/erlang:16.03

MAINTAINER Kazuhiro Suzuki <ksauzzmsg@gmail.com>

RUN git clone git://github.com/basho/basho_bench.git
RUN cd basho_bench && make all

RUN apt-get install --no-install-recommends -y gnuplot
RUN apt-get clean
