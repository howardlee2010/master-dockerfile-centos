FROM kolla/centos-source-openvswitch-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="openvswitch-netcontrold" build-date="20200211"











RUN yum -y install python3-pip \
    && yum clean all && rm -rf /var/cache/yum



RUN pip3 --no-cache-dir install --upgrade netcontrold





COPY extend_start.sh /usr/local/bin/kolla_openvswitch_extend_start
RUN chmod 755 /usr/local/bin/kolla_openvswitch_extend_start


