FROM kolla/centos-source-prometheus-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="prometheus-haproxy-exporter" build-date="20200211"




ENV haproxy_exporter_version=0.10.0



RUN curl -sSL -o /tmp/haproxy_exporter.tar.gz https://github.com/prometheus/haproxy_exporter/releases/download/v${haproxy_exporter_version}/haproxy_exporter-${haproxy_exporter_version}.linux-amd64.tar.gz \
    && tar xvf /tmp/haproxy_exporter.tar.gz -C /opt/ \
    && rm -f /tmp/haproxy_exporter.tar.gz \
    && ln -s /opt/haproxy_exporter* /opt/haproxy_exporter





USER prometheus