FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="multipathd" build-date="20200211"






    


RUN yum -y install device-mapper-multipath \
    && yum clean all && rm -rf /var/cache/yum


