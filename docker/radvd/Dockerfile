FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="radvd" build-date="20200211"






RUN yum -y install radvd \
    && yum clean all && rm -rf /var/cache/yum


