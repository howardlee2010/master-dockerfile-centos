FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="rsyslog-base" build-date="20200211"







RUN yum -y install rsyslog \
    && yum clean all && rm -rf /var/cache/yum


