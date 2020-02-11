FROM kolla/centos-source-cinder-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-backup" build-date="20200211"






    
        
     



RUN yum -y install nfs-utils \
    && yum clean all && rm -rf /var/cache/yum




USER cinder