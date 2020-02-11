FROM kolla/centos-source-neutron-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-linuxbridge-agent" build-date="20200211"







    
    
        
    



RUN yum -y install ebtables bridge-utils \
    && yum clean all && rm -rf /var/cache/yum




USER neutron