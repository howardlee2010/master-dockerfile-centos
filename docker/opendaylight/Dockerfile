FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="opendaylight" build-date="20200211"








RUN usermod --append --home /var/lib/odl --groups kolla odl \
    && mkdir -p /var/lib/odl \
    && chown -R 42462:42462 /var/lib/odl




RUN yum-config-manager  --enable opendaylight






    


RUN yum -y install java-1.8.0-openjdk-headless opendaylight \
    && yum clean all && rm -rf /var/cache/yum



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


