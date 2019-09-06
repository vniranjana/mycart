#This is dockerfile for mycart MS Front end layer
FROM centos:7
MAINTAINER vniranjana@gmail.com
RUN yum -y update
ADD config /opt
RUN yum -y install `cat /opt/packages`
RUN yum -y install `cat /opt/myapp-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]





