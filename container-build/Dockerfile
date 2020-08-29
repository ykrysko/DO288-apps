# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
LABEL io.openshift.tags="Apache, httpd" \
      io.k8s.description="My first Apache RHOCP app" \
      io.openshift.expose-services="8080:http"
RUN sed -i "s|Listen 80|Listen 8080|g" /etc/httpd/conf/httpd.conf
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R u=g /var/run/httpd /var/log/httpd
USER 1001
EXPOSE 8080
