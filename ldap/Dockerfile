FROM smartdeveloperhub/ldap
MAINTAINER Alejandro F. Carrera <alej4fc@gmail.com>

ADD ./ldap.ldif /ldap.ldif
RUN ldapadd -c -D "cn=admin,dc=ldap,dc=smartdeveloperhub,dc=org" -w ldapsdh12345 -f /ldap.ldif

EXPOSE 80 389 636
