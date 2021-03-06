FROM centos:7
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="base" build-date="20200211"


# NOTE(yoctozepto): use a UTF-8 (Unicode) locale like standard image installs do
# fixes issues arising from ascii fallback usage
ENV LANG en_US.UTF-8




RUN groupadd --force --gid 42475 almanach \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42475 --gid 42475 almanach \
    && groupadd --force --gid 42401 ansible \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42401 --gid 42401 ansible \
    && groupadd --force --gid 42402 aodh \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42402 --gid 42402 aodh \
    && groupadd --force --gid 42403 barbican \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42403 --gid 42403 barbican \
    && groupadd --force --gid 42404 bifrost \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42404 --gid 42404 bifrost \
    && groupadd --force --gid 42471 blazar \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42471 --gid 42471 blazar \
    && groupadd --force --gid 42405 ceilometer \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42405 --gid 42405 ceilometer \
    && groupadd --force --gid 64045 ceph \
    && useradd -l -M --shell /usr/sbin/nologin --uid 64045 --gid 64045 ceph \
    && groupadd --force --gid 42406 chrony \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42406 --gid 42406 chrony \
    && groupadd --force --gid 42407 cinder \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42407 --gid 42407 cinder \
    && groupadd --force --gid 42408 cloudkitty \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42408 --gid 42408 cloudkitty \
    && groupadd --force --gid 42409 collectd \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42409 --gid 42409 collectd \
    && groupadd --force --gid 42410 congress \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42410 --gid 42410 congress \
    && groupadd --force --gid 42483 cyborg \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42483 --gid 42483 cyborg \
    && groupadd --force --gid 42411 designate \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42411 --gid 42411 designate \
    && groupadd --force --gid 42464 dragonflow \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42464 --gid 42464 dragonflow \
    && groupadd --force --gid 42466 ec2api \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42466 --gid 42466 ec2api \
    && groupadd --force --gid 42412 elasticsearch \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42412 --gid 42412 elasticsearch \
    && groupadd --force --gid 42413 etcd \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42413 --gid 42413 etcd \
    && groupadd --force --gid 42474 fluentd \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42474 --gid 42474 fluentd \
    && groupadd --force --gid 42414 freezer \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42414 --gid 42414 freezer \
    && groupadd --force --gid 42415 glance \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42415 --gid 42415 glance \
    && groupadd --force --gid 42416 gnocchi \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42416 --gid 42416 gnocchi \
    && groupadd --force --gid 42417 grafana \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42417 --gid 42417 grafana \
    && groupadd --force --gid 42454 haproxy \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42454 --gid 42454 haproxy \
    && groupadd --force --gid 42418 heat \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42418 --gid 42418 heat \
    && groupadd --force --gid 42420 horizon \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42420 --gid 42420 horizon \
    && groupadd --force --gid 42477 hugetlbfs \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42477 --gid 42477 hugetlbfs \
    && groupadd --force --gid 42421 influxdb \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42421 --gid 42421 influxdb \
    && groupadd --force --gid 42422 ironic \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42422 --gid 42422 ironic \
    && groupadd --force --gid 42461 ironic-inspector \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42461 --gid 42461 ironic-inspector \
    && groupadd --force --gid 42423 kafka \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42423 --gid 42423 kafka \
    && groupadd --force --gid 42458 karbor \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42458 --gid 42458 karbor \
    && groupadd --force --gid 42425 keystone \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42425 --gid 42425 keystone \
    && groupadd --force --gid 42426 kibana \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42426 --gid 42426 kibana \
    && groupadd --force --gid 42400 kolla \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42400 --gid 42400 kolla \
    && groupadd --force --gid 42469 kuryr \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42469 --gid 42469 kuryr \
    && groupadd --force --gid 42473 libvirt \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42473 --gid 42473 libvirt \
    && groupadd --force --gid 42478 logstash \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42478 --gid 42478 logstash \
    && groupadd --force --gid 42428 magnum \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42428 --gid 42428 magnum \
    && groupadd --force --gid 42429 manila \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42429 --gid 42429 manila \
    && groupadd --force --gid 42485 masakari \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42485 --gid 42485 masakari \
    && groupadd --force --gid 42457 memcached \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42457 --gid 42457 memcached \
    && groupadd --force --gid 42430 mistral \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42430 --gid 42430 mistral \
    && groupadd --force --gid 42431 monasca \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42431 --gid 42431 monasca \
    && groupadd --force --gid 65534 mongodb \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42432 --gid 65534 mongodb \
    && groupadd --force --gid 42433 murano \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42433 --gid 42433 murano \
    && groupadd --force --gid 42434 mysql \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42434 --gid 42434 mysql \
    && groupadd --force --gid 42435 neutron \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42435 --gid 42435 neutron \
    && groupadd --force --gid 42481 nfast \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42481 --gid 42481 nfast \
    && groupadd --force --gid 42436 nova \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42436 --gid 42436 nova \
    && groupadd --force --gid 42470 novajoin \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42470 --gid 42470 novajoin \
    && groupadd --force --gid 42437 octavia \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42437 --gid 42437 octavia \
    && groupadd --force --gid 42462 odl \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42462 --gid 42462 odl \
    && groupadd --force --gid 42476 openvswitch \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42476 --gid 42476 openvswitch \
    && groupadd --force --gid 42438 panko \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42438 --gid 42438 panko \
    && groupadd --force --gid 42482 placement \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42482 --gid 42482 placement \
    && groupadd --force --gid 42472 prometheus \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42472 --gid 42472 prometheus \
    && groupadd --force --gid 42465 qdrouterd \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42465 --gid 42465 qdrouterd \
    && groupadd --force --gid 42427 qemu \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42427 --gid 42427 qemu \
    && groupadd --force --gid 42484 qinling \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42484 --gid 42484 qinling \
    && groupadd --force --gid 42439 rabbitmq \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42439 --gid 42439 rabbitmq \
    && groupadd --force --gid 42440 rally \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42440 --gid 42440 rally \
    && groupadd --force --gid 42460 redis \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42460 --gid 42460 redis \
    && groupadd --force --gid 42441 sahara \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42441 --gid 42441 sahara \
    && groupadd --force --gid 42442 searchlight \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42442 --gid 42442 searchlight \
    && groupadd --force --gid 42443 senlin \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42443 --gid 42443 senlin \
    && groupadd --force --gid 42467 sensu \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42467 --gid 42467 sensu \
    && groupadd --force --gid 42468 skydive \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42468 --gid 42468 skydive \
    && groupadd --force --gid 42444 solum \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42444 --gid 42444 solum \
    && groupadd --force --gid 42479 storm \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42479 --gid 42479 storm \
    && groupadd --force --gid 42445 swift \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42445 --gid 42445 swift \
    && groupadd --force --gid 42446 tacker \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42446 --gid 42446 tacker \
    && groupadd --force --gid 42447 td-agent \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42447 --gid 42447 td-agent \
    && groupadd --force --gid 42448 telegraf \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42448 --gid 42448 telegraf \
    && groupadd --force --gid 42480 tempest \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42480 --gid 42480 tempest \
    && groupadd --force --gid 42449 trove \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42449 --gid 42449 trove \
    && groupadd --force --gid 42459 vitrage \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42459 --gid 42459 vitrage \
    && groupadd --force --gid 42450 vmtp \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42450 --gid 42450 vmtp \
    && groupadd --force --gid 42451 watcher \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42451 --gid 42451 watcher \
    && groupadd --force --gid 42452 zaqar \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42452 --gid 42452 zaqar \
    && groupadd --force --gid 42453 zookeeper \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42453 --gid 42453 zookeeper \
    && groupadd --force --gid 42463 zun \
    && useradd -l -M --shell /usr/sbin/nologin --uid 42463 --gid 42463 zun

LABEL kolla_version="9.1.0"




ENV KOLLA_BASE_DISTRO=centos \
    KOLLA_INSTALL_TYPE=source \
    KOLLA_INSTALL_METATYPE=mixed \
    KOLLA_DISTRO_PYTHON_VERSION=2.7 \
    KOLLA_BASE_ARCH=x86_64


#### Customize PS1 to be used with bash shell
COPY kolla_bashrc /tmp/
RUN cat /tmp/kolla_bashrc >> /etc/skel/.bashrc \
    && cat /tmp/kolla_bashrc >> /root/.bashrc

# PS1 var when used /bin/sh shell
ENV PS1="$(tput bold)($(printenv KOLLA_SERVICE_NAME))$(tput sgr0)[$(id -un)@$(hostname -s) $(pwd)]$ "


# For RPM Variants, enable the correct repositories - this should all be done
# in the base image so repos are consistent throughout the system.  This also
# enables to provide repo overrides at a later date in a simple fashion if we
# desire such functionality.  I think we will :)



RUN CURRENT_DISTRO_RELEASE=$(awk '{match($0, /[0-9]+/,version)}END{print version[0]}' /etc/system-release); \
    if [  $CURRENT_DISTRO_RELEASE != "7" ] && [ $CURRENT_DISTRO_RELEASE != 8 ]; then \
        echo "Only releases '7' and '8' are supported on centos"; false; \
    fi \
    && cat /tmp/kolla_bashrc >> /etc/bashrc \
    && sed -i 's|^\(override_install_langs=.*\)|# \1|' /etc/yum.conf




COPY yum.conf /etc/yum.conf




# Install what is needed for en_US.UTF-8






#### BEGIN REPO ENABLEMENT







    
    # FIXME(mgoddard): Not available for CentOS 8 yet.
    
        
    

    
    # FIXME(mgoddard): Not available for CentOS 8 yet.
    
        
    

COPY grafana.repo /etc/yum.repos.d/grafana.repo
COPY influxdb.repo /etc/yum.repos.d/influxdb.repo
COPY rabbitmq_rabbitmq-server.repo /etc/yum.repos.d/rabbitmq_rabbitmq-server.repo
COPY td.repo /etc/yum.repos.d/td.repo
COPY crmsh.repo /etc/yum.repos.d/crmsh.repo
COPY elasticsearch.repo /etc/yum.repos.d/elasticsearch.repo
COPY opendaylight.repo /etc/yum.repos.d/opendaylight.repo

# NOTE(hrw): 'rabbitmq-server' is 'noarch' so we can install it on ppc64le from
# repo for other architecture.
# NOTE(mjturek): tripleo-ci overrides these repos so the file would not exist
# in that case. We test for the file's existence to avoid sed failing in that case.






RUN rpm --import https://packages.grafana.com/gpg.key \
    && rpm --import https://repos.influxdata.com/influxdb.key \
    && rpm --import https://packages.treasuredata.com/GPG-KEY-td-agent \
    && rpm --import https://artifacts.elastic.co/GPG-KEY-elasticsearch



RUN curl -L https://trunk.rdoproject.org/centos7/current-passed-ci/delorean.repo -o /etc/yum.repos.d/delorean.repo

RUN curl -L https://trunk.rdoproject.org/centos7/delorean-deps.repo -o /etc/yum.repos.d/delorean-deps.repo




    
    

    

    



RUN rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7




# FIXME(mgoddard): Not available for CentOS 8 yet.

    



# FIXME(mgoddard): Not available for CentOS 8 yet.

    
# FIXME(mnasiadka): Replace with CentOS Storage SIG packages when avail



    



# FIXME(mgoddard): Not available for CentOS 8 yet.

    


RUN yum -y install epel-release centos-release-ceph-nautilus centos-release-opstools centos-release-qemu-ev yum-plugin-priorities \
    && yum-config-manager --disable influxdb \
    && yum-config-manager --disable centos-ceph-nautilus \
    && yum-config-manager --disable centos-nfs-ganesha28 \
    && yum-config-manager --disable centos-qemu-ev \
&& rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-SIG-OpsTools \
&& rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-SIG-Storage \
&& rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-SIG-Virtualization \
&& yum -y update --security --sec-severity=Important --sec-severity=Critical \
    && yum clean all && rm -rf /var/cache/yum
    

    
    

#### END REPO ENABLEMENT







    


    


# Install base packages
RUN yum -y install ca-certificates curl findutils iproute iscsi-initiator-utils lvm2 ncurses procps-ng socat sudo tar which python scsi-target-utils \
    && yum clean all && rm -rf /var/cache/yum










RUN sed -ri '/-session(\s+)optional(\s+)pam_systemd.so/d' /etc/pam.d/system-auth


COPY set_configs.py /usr/local/bin/kolla_set_configs

COPY start.sh /usr/local/bin/kolla_start
COPY copy_cacerts.sh /usr/local/bin/kolla_copy_cacerts
COPY httpd_setup.sh /usr/local/bin/kolla_httpd_setup
COPY sudoers /etc/sudoers
COPY curlrc /root/.curlrc





RUN curl -sSL https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64 -o /usr/local/bin/dumb-init \
    && chmod +x /usr/local/bin/dumb-init



ENTRYPOINT ["dumb-init", "--single-child", "--"]






COPY healthcheck_curl healthcheck_filemod healthcheck_listen healthcheck_port healthcheck_socket /usr/local/bin/
RUN chmod 755 /usr/local/bin/healthcheck_*




RUN touch /usr/local/bin/kolla_extend_start \
    && chmod 755 /usr/local/bin/kolla_start /usr/local/bin/kolla_extend_start /usr/local/bin/kolla_set_configs /usr/local/bin/kolla_copy_cacerts /usr/local/bin/kolla_httpd_setup \
    && chmod 440 /etc/sudoers \
    && mkdir -p /var/log/kolla \
    && chown :kolla /var/log/kolla \
    && chmod 2775 /var/log/kolla \
    && rm -f /tmp/kolla_bashrc


CMD ["kolla_start"]