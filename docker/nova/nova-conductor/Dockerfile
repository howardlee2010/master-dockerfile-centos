FROM kolla/centos-source-nova-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-conductor" build-date="20200211"







COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start




USER nova