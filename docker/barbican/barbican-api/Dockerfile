FROM kolla/centos-source-barbican-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="barbican-api" build-date="20200211"







COPY extend_start.sh /usr/local/bin/kolla_barbican_extend_start

RUN chmod 755 /usr/local/bin/kolla_barbican_extend_start




USER barbican