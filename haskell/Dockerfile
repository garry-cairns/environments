FROM ubuntu:14.04

# update packages and prepare to build software
RUN apt-get update
RUN apt-get -y install build-essential libgmp3-dev vim git wget

# install latest ghc
RUN wget https://www.haskell.org/platform/download/2014.2.0.0/haskell-platform-2014.2.0.0-unknown-linux-x86_64.tar.gz 
RUN tar xvf ./haskell-platform-2014.2.0.0-unknown-linux-x86_64.tar.gz
RUN /usr/local/haskell/ghc-7.8.3-x86_64/bin/activate-hs

EXPOSE 3000
