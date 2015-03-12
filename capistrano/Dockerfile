FROM base/arch

MAINTAINER KF Interactive pw@kf-interactive.com

RUN pacman -Syu --noconfirm && pacman-db-upgrade
RUN pacman -S git ruby --noconfirm
RUN gem install capistrano -n /usr/local/sbin --version=3.3.5

WORKDIR /project-root
