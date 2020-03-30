# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

USER 1001

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf
EXPOSE 8080
RUN chgrp -R - /var/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd

LABEL io.openshift.expose-services="8080:http"
LABEL io.k8s.description="A basic Apache HTTP Server child image, uses ONBUILD"
LABEL io.k8s.display-name="Apache HTTP Server"
LABEL io.openshift.tags="apache, httpd"
