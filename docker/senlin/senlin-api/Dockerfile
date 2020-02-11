FROM kolla/centos-source-senlin-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="senlin-api" build-date="20200211"







COPY extend_start.sh /usr/local/bin/kolla_senlin_extend_start
RUN chmod 755 /usr/local/bin/kolla_senlin_extend_start




USER senlin