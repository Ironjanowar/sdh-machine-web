FROM alejandrofcarrera/phusion.node
MAINTAINER Alejandro F. Carrera

# Configure runit
ADD ./my_init.d/ /etc/my_init.d/
ONBUILD ./my_init.d/ /etc/my_init.d/

CMD ["/sbin/my_init"]

WORKDIR /usr/lib

EXPOSE 8080
