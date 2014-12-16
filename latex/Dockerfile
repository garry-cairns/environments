FROM ubuntu:14.04

# update packages and prepare to build software
RUN apt-get update
RUN apt-get -y install build-essential vim git wget

# install latex packages
RUN apt-get -y install tex-common texlive-base texlive-binaries texlive-extra-utils texlive-font-utils texlive-fonts-recommended texlive-generic-recommended texlive-latex-base texlive-latex-base-doc texlive-latex-extra texlive-latex-recommended texlive-latex-recommended-doc texlive-luatex texlive-pictures texlive-pstricks texlive-pstricks-doc
