FROM kolla/centos-source-nova-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-novncproxy" build-date="20200211"







        



RUN yum -y install novnc \
    && yum clean all && rm -rf /var/cache/yum




USER nova