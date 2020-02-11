FROM kolla/centos-source-openstack-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="collectd" build-date="20200211"








RUN usermod --append --home /var/lib/collectd --groups kolla collectd \
    && mkdir -p /var/lib/collectd \
    && chown -R 42409:42409 /var/lib/collectd





  

  
  
  

  
      
  

  
    
      
    

  


RUN yum -y install collectd collectd-apache collectd-bind collectd-ceph collectd-chrony collectd-curl collectd-curl_json collectd-curl_xml collectd-dbi collectd-disk collectd-dns collectd-generic-jmx collectd-ipmi collectd-log_logstash collectd-mcelog collectd-memcachec collectd-mysql collectd-netlink collectd-openldap collectd-ping collectd-python collectd-sensors collectd-sensubility collectd-smart collectd-snmp collectd-utils collectd-virt collectd-write_http collectd-write_kafka collectd-write_prometheus collectd-amqp1 collectd-connectivity collectd-ovs-events collectd-ovs-stats collectd-procevent collectd-snmp-agent collectd-sysevent python-collectd-gnocchi python2-collectd-rabbitmq-monitoring python2-sqlalchemy-collectd collectd-iptables collectd-hugepages collectd-pmu collectd-rdt collectd-turbostat \
    && yum clean all && rm -rf /var/cache/yum

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start \
    && chown -R collectd /var/lib/collectd \
    && chown -R collectd /etc/collectd* \
    && chown -R collectd /var/run/




USER collectd