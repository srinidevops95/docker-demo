FROM centos

MAINTAINER <Srini>

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && \
    sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-* && \

    yum -y update && \

   yum -y install httpd 

COPY index.html /var/www/html/

EXPOSE 80

ENTRYPOINT ["/usr/sbin/httpd"]
CMD ["-D", "FOREGROUND"]

#CMD [“/usr/sbin/httpd”, “-D”, “FOREGROUND”]

