FROM owasp/modsecurity:3-apache

ENV DEBIAN_FRONTEND noninteractive

COPY ./conf/REQUEST-912-DOS-PROTECTION.conf /etc/modsecurity.d/rules/
COPY ./conf/crs-setup.conf /etc/modsecurity.d/
COPY ./conf/modsecurity.conf /etc/modsecurity.d/