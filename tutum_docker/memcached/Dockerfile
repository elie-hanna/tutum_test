FROM tutum.co/eliehanna/centos:6.6

MAINTAINER Elie Hanna <elie.hanna@elementn.com>

ENV HOME /root

### Change the shell to bash (easier to work in a bash shell...)
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

RUN yum install -y memcached

COPY ./memcached-sysconfig /etc/sysconfig/memcached

EXPOSE 11211

CMD /etc/init.d/memcached start && \
	ping -i 3600 localhost

