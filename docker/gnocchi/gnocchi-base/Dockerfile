FROM kolla/centos-source-openstack-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="gnocchi-base" build-date="20200211"








RUN usermod --append --home /var/lib/gnocchi --groups kolla gnocchi \
    && mkdir -p /var/lib/gnocchi \
    && chown -R 42416:42416 /var/lib/gnocchi


# FIXME(mnasiadka): Remove when CentOS Storage SIG repo is available for CentOS 8

    

RUN yum-config-manager  --enable centos-ceph-nautilus





    

       
        
       
        


        # on x86-64 pip grabs precompiled numpy/scipy - on aarch64/ppc64le
        # it needs to be built

        

RUN yum -y install httpd librados2-devel mod_ssl mod_wsgi python2-ldappool \
    && yum clean all && rm -rf /var/cache/yum
RUN mkdir -p /var/www/cgi-bin/gnocchi \
    && sed -i -r 's,^(Listen 80),#\1,' /etc/httpd/conf/httpd.conf \
    && sed -i -r 's,^(Listen 443),#\1,' /etc/httpd/conf.d/ssl.conf
    
ADD gnocchi-base-archive /gnocchi-base-source



RUN ln -s gnocchi-base-source/* gnocchi \
    && pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt gnocchiclient /gnocchi[keystone,mysql,file,ceph,s3] \
    && mkdir -p /etc/gnocchi \
    && chown -R gnocchi: /etc/gnocchi



COPY extend_start.sh /usr/local/bin/kolla_extend_start
COPY gnocchi_sudoers /etc/sudoers.d/kolla_gnocchi_sudoers

RUN chmod 750 /etc/sudoers.d \
    && chmod 640 /etc/sudoers.d/kolla_gnocchi_sudoers \
    && touch /usr/local/bin/kolla_gnocchi_extend_start \
    && chmod 755 /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_gnocchi_extend_start

