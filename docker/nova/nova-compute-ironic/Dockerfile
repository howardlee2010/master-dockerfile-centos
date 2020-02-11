FROM kolla/centos-source-nova-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-compute-ironic" build-date="20200211"









RUN yum -y install genisoimage \
    && yum clean all && rm -rf /var/cache/yum






USER nova