FROM kolla/centos-source-ovn-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="ovn-nb-db-server" build-date="20200211"






    


RUN yum -y install openvswitch-ovn-central \
    && yum clean all && rm -rf /var/cache/yum

COPY start_nb_db_server.sh /usr/local/bin/start-nb-db-server
RUN chmod 755 /usr/local/bin/start-nb-db-server


