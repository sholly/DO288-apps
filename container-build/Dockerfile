# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
LABEL io.openshift.expose-services="8080:http"
LABEL io.kos.description="http server" \
io.k8s.display-name="Apache HTTP Serer" \ 
io.openshift.tags="apache, httpd" \ 
io.openshift.expose-services="8080:http" 

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \ 
chmod -R g=u /var/lot/httpd /var/run/httpd

USER 1001 

