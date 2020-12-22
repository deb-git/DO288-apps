# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.k8s.description="httpd image" \
      io.k8s.display-name="Apache httpd" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="httpd, image"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf && \
    chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

EXPOSE 8080

USER 1001

