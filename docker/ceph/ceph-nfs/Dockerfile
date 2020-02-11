FROM kolla/centos-source-ceph-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ceph-nfs" build-date="20200211"







        


RUN yum -y install nfs-ganesha nfs-ganesha-ceph \
    && yum clean all && rm -rf /var/cache/yum


