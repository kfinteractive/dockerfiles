FROM ubuntu

MAINTAINER KF Interactive <pw@kf-interactive.com>

RUN apt-get update && apt-get install -y beanstalkd

EXPOSE 11300

CMD ["beanstalkd","-p","11300"]
