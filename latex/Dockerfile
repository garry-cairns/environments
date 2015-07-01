FROM ubuntu:14.04
MAINTAINER Garry Cairns
ENV REFRESHED_AT 2014-12-28

# update packages and prepare to build software
RUN ["apt-get", "update"]
RUN ["apt-get", "-y", "install", "build-essential", "vim", "git", "wget"]
RUN ["locale-gen", "en_GB.UTF-8"]

# install latex packages
RUN ["apt-get", "-y", "install", "tex-common", "texlive-base", "texlive-binaries", "texlive-extra-utils", "texlive-font-utils", "texlive-fonts-recommended", "texlive-generic-recommended", "texlive-latex-base", "texlive-latex-base-doc", "texlive-latex-extra", "texlive-latex-recommended", "texlive-latex-recommended-doc", "texlive-luatex", "texlive-pictures", "texlive-pstricks", "texlive-pstricks-doc"]

# create a latex user to run our programs
RUN ["groupadd", "-r", "latex"]
RUN ["useradd", "-r", "-g", "latex", "latex"]
WORKDIR /home/latex
RUN ["touch", ".bashrc"]

# uncomment the line below to use container as a non-root user
# USER latex:latex
