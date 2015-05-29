FROM horie/centos7:1.0

RUN yum install -y epel-release
RUN rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm

RUN yum install -y httpd mysql vim
RUN yum install -y php php-mbstring php-mysql php-devel php-mcrypt
EXPOSE 3306
