FROM ubuntu:latest

MAINTAINER KFI pw@kf-interactive.com

RUN apt-get update && apt-get install -y make gcc python python-dev python-setuptools

RUN easy_install -U Sphinx
RUN easy_install -U sphinxcontrib-seqdiag
RUN easy_install -U sphinxcontrib-blockdiag
RUN easy_install -U sphinxcontrib-httpdomain
RUN easy_install -U sphinxcontrib-phpdomain


WORKDIR /doc
