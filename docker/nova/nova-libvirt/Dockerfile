FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="nova-libvirt" build-date="20200211"








RUN usermod --append --home /var/lib/nova --groups kolla nova \
    && usermod --append --groups qemu nova \
    && mkdir -p /var/lib/nova \
    && chown -R 42436:42436 /var/lib/nova


# FIXME(mnasiadka): Remove when CentOS Storage SIG repo is available for CentOS 8

    

RUN yum-config-manager  --enable centos-ceph-nautilus






    
    
        
    
    
        
    

    
        
            
        
    



RUN yum -y install ceph-common cyrus-sasl-scram libguestfs libvirt-client libvirt-daemon libvirt-daemon-config-nwfilter libvirt-daemon-driver-nwfilter openvswitch trousers qemu-kvm-ev libvirt-daemon-driver-lxc OVMF \
    && yum clean all && rm -rf /var/cache/yum



    
# NOTE(jeffrey4l): for x86_64, nova will validate the existence of /usr/share/OVMF/OVMF_CODE.fd
RUN ln -sf /usr/share/OVMF/OVMF_CODE.secboot.fd /usr/share/OVMF/OVMF_CODE.fd
    



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


