FROM kolla/centos-source-openstack-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="glance-base" build-date="20200211"








RUN usermod --append --home /var/lib/glance --groups kolla glance \
    && mkdir -p /var/lib/glance \
    && chown -R 42415:42415 /var/lib/glance


# FIXME(mnasiadka): Remove when CentOS Storage SIG repo is available for CentOS 8

    

RUN yum-config-manager  --enable centos-ceph-nautilus





    
        
        
        
    

RUN yum -y install python-rados python-rbd \
    && yum clean all && rm -rf /var/cache/yum

ADD glance-base-archive /glance-base-source



RUN ln -s glance-base-source/* glance \
    && pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /glance glance_store[cinder,vmware,swift] \
    && mkdir -p /etc/glance \
    && cp -r /glance/etc/* /etc/glance/ \
    && chown -R glance: /etc/glance



COPY extend_start.sh /usr/local/bin/kolla_extend_start

RUN touch /usr/local/bin/kolla_glance_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_glance_extend_start

