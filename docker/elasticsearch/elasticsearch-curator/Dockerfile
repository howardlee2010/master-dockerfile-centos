FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="elasticsearch-curator" build-date="20200211"






    


RUN yum -y install cronie python3-pip \
    && yum clean all && rm -rf /var/cache/yum




RUN usermod --append --home /var/lib/elasticsearch --groups kolla elasticsearch \
    && mkdir -p /var/lib/elasticsearch \
    && chown -R 42412:42412 /var/lib/elasticsearch




RUN pip3 --no-cache-dir install --upgrade elasticsearch-curator \
    && mkdir -p /etc/elasticsearch-curator \
    && chown -R elasticsearch: /etc/elasticsearch-curator

COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




# NOTE(dszumski): Cron runs as root but should be configured to launch Curator
# by the elasticsearch user.