FROM kolla/centos-source-ceilometer-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceilometer-ipmi" build-date="20200211"






    
        
    



RUN yum -y install ipmitool \
    && yum clean all && rm -rf /var/cache/yum




USER ceilometer