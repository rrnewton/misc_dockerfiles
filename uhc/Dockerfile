FROM ubuntu:14.04

RUN apt-get update && \
    apt-get install -y wget make libgmp3-dev

RUN wget http://foswiki.cs.uu.nl/foswiki/pub/UHC/Download/uhc-1.1.3-2432M-20120203-64-x86_64-unknown-linux-gnu.tar.bz2 && \
    tar xf uhc-1.1.3-2432M-20120203-64-x86_64-unknown-linux-gnu.tar.bz2 && \
    rm uhc-1.1.3-2432M-20120203-64-x86_64-unknown-linux-gnu.tar.bz2 && \
    mv uhc-1.1.3-2432M-20120203-64-x86_64-unknown-linux-gnu uhc

RUN cd uhc && ./configure
RUN cd uhc && make
RUN cd uhc && make install

# RUN cd uhc && make test
