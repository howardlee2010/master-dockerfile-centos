FROM kolla/centos-source-searchlight-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="searchlight-api" build-date="20200211"





COPY extend_start.sh /usr/local/bin/kolla_searchlight_extend_start
RUN chmod 755 /usr/local/bin/kolla_searchlight_extend_start




USER searchlight