FROM kolla/centos-source-redis-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="redis-sentinel" build-date="20200211"






    

RUN yum -y install redis \
    && yum clean all && rm -rf /var/cache/yum




USER redis