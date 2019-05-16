FROM owasp/modsecurity:3-apache

ENV DEBIAN_FRONTEND noninteractive

WORKDIR /scripts

COPY ./conf/REQUEST-912-DOS-PROTECTION.conf /etc/modsecurity.d/rules/
COPY ./conf/crs-setup.conf /etc/modsecurity.d/
COPY ./conf/modsecurity.conf /etc/modsecurity.d/

COPY ./conf/iptables_rules.sh /scripts/iptables_rules.sh
RUN chmod u+x /scripts/iptables_rules.sh

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y apt-utils && \
    apt-get install -y --no-install-recommends iptables && \
    apt-get autoremove -y