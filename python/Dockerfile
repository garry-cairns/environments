FROM ubuntu:14.04

# update packages and prepare to build software
RUN apt-get update
RUN apt-get -y install build-essential vim git wget

# install latest python
RUN apt-get -y build-dep python3-dev python3-imaging
RUN apt-get -y install python3-dev python3-imaging python3-pip

# install common python libraries
RUN pip3 install django djangorestframework cookiecutter
RUN pip3 install pandas ipython
