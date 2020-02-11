FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="skydive-base" build-date="20200211"








RUN usermod --append --home /var/lib/skydive --groups kolla skydive \
    && mkdir -p /var/lib/skydive \
    && chown -R 42468:42468 /var/lib/skydive





RUN curl -o /usr/bin/skydive -L "https://github.com/skydive-project/skydive/releases/download/v0.26.0/skydive" \
    && chmod +x /usr/bin/skydive




COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


