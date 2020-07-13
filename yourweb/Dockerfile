FROM	ubi7/ubi

EXPOSE	8080

RUN	yum install -y httpd; \
	yum clean all; \
	sed -ie 's/Listen 80/Listen 8080/' /etc/httpd/conf/httpd.conf; \
	echo hello world > /var/www/html/index.html

USER	apache

ENTRYPOINT httpd -DFOREGROUND
