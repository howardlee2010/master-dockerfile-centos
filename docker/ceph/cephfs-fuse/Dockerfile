FROM kolla/centos-source-ceph-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="cephfs-fuse" build-date="20200211"






# Clear any customisation by Kolla to entrypoint & command
ENTRYPOINT ["/usr/bin/ceph-fuse"]
CMD []