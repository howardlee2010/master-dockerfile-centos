FROM kolla/centos-source-octavia-base:9.1.0
LABEL maintainer="Kolla Project (https://launchpad.net/kolla)" name="octavia-api" build-date="20200211"






    
        
        
        
        

    



RUN yum -y install httpd mod_ssl mod_wsgi \
    && yum clean all && rm -rf /var/cache/yum


RUN sed -i -r 's,^(Listen 80),#\1,' /etc/httpd/conf/httpd.conf \
            && sed -i -r 's,^(Listen 443),#\1,' /etc/httpd/conf.d/ssl.conf


COPY extend_start.sh /usr/local/bin/kolla_octavia_extend_start
RUN chmod 755 /usr/local/bin/kolla_octavia_extend_start




USER octavia