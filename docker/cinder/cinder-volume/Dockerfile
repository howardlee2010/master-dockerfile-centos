FROM kolla/centos-source-cinder-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cinder-volume" build-date="20200211"






    
    
    
    
RUN yum -y install nfs-utils nvmetcli sysfsutils targetcli python-rtslib python2-cinderlib \
    && yum clean all && rm -rf /var/cache/yum



RUN sed -i '1 i include /var/lib/cinder/volumes/*' /etc/tgt/tgtd.conf







COPY cinder_sudoers /etc/sudoers.d/kolla_cinder_volume_sudoers
COPY extend_start.sh /usr/local/bin/kolla_cinder_extend_start

RUN chmod 750 /etc/sudoers.d \
    && chmod 440 /etc/sudoers.d/kolla_cinder_volume_sudoers \
    && chmod 755 /usr/local/bin/kolla_cinder_extend_start




USER cinder