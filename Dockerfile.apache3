FROM httpd:2.4

WORKDIR /scripts

ENV DEBIAN_FRONTEND noninteractive

COPY ./conf/iptables_rules.sh /scripts/iptables_rules.sh
RUN chmod u+x /scripts/iptables_rules.sh

RUN apt-get update && \
    apt-get dist-upgrade -y && \
    apt-get install -y apt-utils && \
    apt-get install -y --no-install-recommends iptables && \
    apt-get autoremove -y