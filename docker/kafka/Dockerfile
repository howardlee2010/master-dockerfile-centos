FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="kafka" build-date="20200211"







RUN usermod --append --home /opt/kafka --groups kolla kafka \
    && mkdir -p /opt/kafka \
    && chown -R 42423:42423 /opt/kafka



    


RUN yum -y install java-1.8.0-openjdk-headless \
    && yum clean all && rm -rf /var/cache/yum


ENV kafka_version=2.0.1
ENV kafka_scala_version=2.12
ENV kafka_url=https://archive.apache.org/dist/kafka/${kafka_version}/kafka_${kafka_scala_version}-${kafka_version}.tgz
ENV kafka_pkg_sha512sum=9773a85ef2898b4bae20481df4cfd5488bd195fffd700fcc874a9fa55065f6873f2ee12f46d2f6a6ccb5d5a93ddb7dec19227aef5d39d4f72b545ec63b24bb2f



RUN curl -sSL -o /tmp/kafka.tgz ${kafka_url} \
    && echo "${kafka_pkg_sha512sum} /tmp/kafka.tgz" | sha512sum -c \
    && tar --strip 1 -xvf /tmp/kafka.tgz -C /opt/kafka \
    && rm -f /tmp/kafka.tgz


COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start




USER kafka