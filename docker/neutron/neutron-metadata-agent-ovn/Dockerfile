FROM kolla/centos-source-neutron-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-metadata-agent-ovn" build-date="20200211"







ADD plugins-archive /

    

RUN if [ "$(ls /plugins)" ]; then \
        pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /plugins/*; \
    fi






USER neutron