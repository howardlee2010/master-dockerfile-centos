FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ptp" build-date="20200211"







RUN yum -y install linuxptp \
    && yum clean all && rm -rf /var/cache/yum

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


