FROM centos
MAINTAINER Muhammad Ahsan 

RUN yum -y update
RUN yum -y install httpd

EXPOSE 80
CMD ["/usr/sbin/apachectl", "-D","FOREGROUND"]
