FROM ubuntu:14.04
MAINTAINER Garry Cairns
ENV REFRESHED_AT 2014-12-20

# update packages and prepare to build software
RUN ["apt-get", "update"]
RUN ["apt-get", "-y", "install", "build-essential", "vim", "git", "wget"]
RUN ["locale-gen", "en_GB.UTF-8"]

# install latest python
RUN ["apt-get", "-y", "build-dep", "python3-dev", "python3-imaging"]
RUN ["apt-get", "-y", "install", "python3-dev", "python3-imaging", "python3-pip"]

# install common python libraries
RUN ["pip3", "install", "django", "djangorestframework", "cookiecutter"]
RUN ["pip3", "install", "pandas", "ipython"]

# create a python user to run our programs
RUN ["groupadd", "-r", "python"]
RUN ["useradd", "-r", "-g", "python", "python"]
WORKDIR /home/python
RUN ["touch", ".bashrc"]

# uncomment the line below to use container as a non-root user
# USER python:python
