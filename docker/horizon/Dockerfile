FROM kolla/centos-source-openstack-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="horizon" build-date="20200211"








RUN usermod --append --home /var/lib/horizon --groups kolla horizon \
    && mkdir -p /var/lib/horizon \
    && chown -R 42420:42420 /var/lib/horizon



    

        
        
        
        

RUN yum -y install gettext httpd mod_ssl mod_wsgi \
    && yum clean all && rm -rf /var/cache/yum


RUN sed -i -r 's,^(Listen 80),#\1,' /etc/httpd/conf/httpd.conf \
    && sed -i -r 's,^(Listen 443),#\1,' /etc/httpd/conf.d/ssl.conf


    

ADD horizon-archive /horizon-source
ADD plugins-archive /





# NOTE(hrw): to install horizon from unpacked sources we cannot have it in upper-constraints.txt
RUN ln -s horizon-source/* horizon \
    && sed -i /^horizon=/d /requirements/upper-constraints.txt \
    && pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /horizon \
    && mkdir -p /etc/openstack-dashboard \
    && cp -r /horizon/openstack_dashboard/conf/* /etc/openstack-dashboard/ \
    && cp /horizon/openstack_dashboard/local/local_settings.py.example /etc/openstack-dashboard/local_settings \
    && cp /horizon/manage.py /var/lib/kolla/venv/bin/manage.py \
    && if [ "$(ls /plugins)" ]; then \
           pip --no-cache-dir install --upgrade -c /requirements/upper-constraints.txt /plugins/*; \
       fi \
    && for locale in  /var/lib/kolla/venv/lib/python2.7/site-packages/*/locale; do \
           (cd ${locale%/*} && /var/lib/kolla/venv/bin/django-admin compilemessages) \
       done \
    && chown -R horizon: /etc/openstack-dashboard



COPY extend_start.sh /usr/local/bin/kolla_extend_start
RUN chmod 755 /usr/local/bin/kolla_extend_start


