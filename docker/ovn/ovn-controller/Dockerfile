FROM kolla/centos-source-ovn-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ovn-controller" build-date="20200211"






    


RUN yum -y install openvswitch-ovn-host \
    && yum clean all && rm -rf /var/cache/yum


