FROM kolla/centos-source-designate-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="designate-backend-bind9" build-date="20200211"






   

RUN yum -y install bind \
    && yum clean all && rm -rf /var/cache/yum





RUN mkdir -p /var/lib/kolla/ /var/lib/named/ /run/named \
     && chown -R root: /var/lib/named /run/named \
     && chmod 755 /run/named


