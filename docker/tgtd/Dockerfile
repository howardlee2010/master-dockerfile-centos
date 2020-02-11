FROM kolla/centos-source-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="tgtd" build-date="20200211"








RUN sed -i '1 i include /var/lib/cinder/volumes/*' /etc/tgt/tgtd.conf





