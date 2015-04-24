FROM ubuntu:latest

MAINTAINER KFI pw@kf-interactive.com

RUN apt-get update && apt-get install -y make build-essential python-dev python-pip python-virtualenv libxml2-dev libxslt-dev zlib1g-dev

#RUN  virtualenv --system-site-packages virt && \
RUN pip install --allow-external -U \
Pillow Seqdiag Sphinx sphinxcontrib-seqdiag sphinxcontrib-blockdiag sphinxcontrib-httpdomain sphinxcontrib-phpdomain

WORKDIR /doc
