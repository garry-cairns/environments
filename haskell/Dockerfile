FROM ubuntu:14.04

# update packages and prepare to build software
RUN apt-get update
RUN apt-get -y install build-essential libgmp3-dev vim git wget software-properties-common

# install latest ghc
RUN add-apt-repository -y ppa:hvr/ghc
RUN apt-get update
RUN apt-get install -y cabal-install-1.20 ghc-7.8.3
RUN cat >> ~/.bashrc <<EOF
#RUN export PATH=~/.cabal/bin:/opt/cabal/1.20/bin:/opt/ghc/7.8.3/bin:$PATH EOF
RUN export PATH=~/.cabal/bin:/opt/cabal/1.20/bin:/opt/ghc/7.8.3/bin:$PATH
#RUN cabal update
#RUN cabal install alex happy
