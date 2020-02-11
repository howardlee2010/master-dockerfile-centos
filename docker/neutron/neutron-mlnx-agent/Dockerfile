FROM kolla/centos-source-neutron-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="neutron-mlnx-agent" build-date="20200211"






    




RUN yum -y install libvirt-python python-ethtool \
    && yum clean all && rm -rf /var/cache/yum



    

RUN pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt networking-mlnx






USER neutron