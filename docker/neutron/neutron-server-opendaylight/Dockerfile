FROM kolla/centos-source-neutron-server:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-server-opendaylight" build-date="20200211"

USER root







    

ADD plugins-archive /



RUN if [ "$(ls /plugins)" ]; then \
        sed -i 's|^ceilometer===.*$||g' requirements/upper-constraints.txt \
        && pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /plugins/*; \
    fi






USER neutron