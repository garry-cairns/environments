FROM ubuntu:14.04
MAINTAINER Garry Cairns
ENV REFRESHED_AT 2014-12-20

# update packages and prepare to build software
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "build-essential", "libgmp3-dev", "zlib1g-dev", "vim", "git", "wget", "software-properties-common"]

# install latest ghc and essential tools
RUN ["locale-gen", "en_GB.UTF-8"]
RUN ["add-apt-repository", "-y", "ppa:hvr/ghc"]
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "cabal-install-1.20", "ghc-7.8.3"]
ENV PATH ~/.cabal/bin:/.cabal/bin:/opt/cabal/1.20/bin:/opt/ghc/7.8.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
RUN ["cabal", "update"]
RUN ["cabal", "install", "cabal-install"]
RUN ["cabal", "install", "alex", "happy"]

# create a haskell user to run our programs
RUN ["groupadd", "-r", "haskell"]
RUN ["useradd", "-r", "-g", "haskell", "haskell"]
WORKDIR /home/haskell
RUN ["touch", ".bashrc"]

# uncomment the line below to use container as a non-root user
# USER haskell:haskell
