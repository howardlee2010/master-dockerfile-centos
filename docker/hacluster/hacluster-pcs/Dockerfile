FROM kolla/centos-source-hacluster-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="hacluster-pcs" build-date="20200211"







RUN yum-config-manager  --enable network_ha-clustering_Stable




RUN yum -y install pcs crmsh \
    && yum clean all && rm -rf /var/cache/yum

