FROM kolla/centos-source-congress-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="congress-api" build-date="20200211"



COPY extend_start.sh /usr/local/bin/kolla_congress_extend_start
RUN chmod 755 /usr/local/bin/kolla_congress_extend_start




USER congress