FROM kolla/centos-source-hacluster-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="hacluster-corosync" build-date="20200211"






RUN yum -y install corosync \
    && yum clean all && rm -rf /var/cache/yum

