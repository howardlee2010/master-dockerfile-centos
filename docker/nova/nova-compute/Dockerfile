FROM kolla/centos-source-nova-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-compute" build-date="20200211"





# FIXME(mnasiadka): Remove when CentOS Storage SIG repo is available for CentOS 8

    

RUN yum-config-manager  --enable centos-ceph-nautilus





    

        
        
        
        
        
        
        

    

RUN yum -y install ceph-common device-mapper-multipath dosfstools e2fsprogs genisoimage iscsi-initiator-utils libosinfo nfs-utils openvswitch parted sysfsutils targetcli xfsprogs libvirt-python python-libguestfs python-rtslib qemu-img-ev \
    && yum clean all && rm -rf /var/cache/yum





ADD plugins-archive /
RUN pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt oslo-vmware \
    && if [ "$(ls /plugins)" ]; then \
           pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /plugins/*; \
       fi



COPY extend_start.sh /usr/local/bin/kolla_nova_extend_start
RUN chmod 755 /usr/local/bin/kolla_nova_extend_start \
    && rm -f /etc/machine-id




USER nova