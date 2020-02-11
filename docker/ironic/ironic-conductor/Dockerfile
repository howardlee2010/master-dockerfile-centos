FROM kolla/centos-source-ironic-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ironic-conductor" build-date="20200211"







RUN yum-config-manager  --enable centos-ceph-nautilus




    
        
        # FIXME(mgoddard): Removed shellinabox which is not currently provided
        # by EPEL8.
        
        
        
        
            
        
    



RUN pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt -r /ironic/driver-requirements.txt ironic-staging-drivers


RUN yum -y install dosfstools e2fsprogs fuse gdisk ipmitool openssh-clients parted psmisc util-linux xfsprogs shellinabox systemd-python systemd qemu-img-ev \
    && yum clean all && rm -rf /var/cache/yum




USER ironic