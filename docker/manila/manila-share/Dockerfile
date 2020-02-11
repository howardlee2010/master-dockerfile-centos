FROM kolla/centos-source-manila-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="manila-share" build-date="20200211"





# FIXME(mnasiadka): Remove when CentOS Storage SIG repo is available for CentOS 8

    

RUN yum-config-manager  --enable centos-ceph-nautilus





    
        
    

RUN yum -y install ceph-common sqlite \
    && yum clean all && rm -rf /var/cache/yum






USER manila