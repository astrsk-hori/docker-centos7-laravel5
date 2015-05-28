FROM horie/centos7:1.0
RUN yum install -y httpd.x86_64
RUN yum install -y epel-release
RUN rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
RUN yum install -y --enablerepo=remi php54-php.x86_64 php54-php-devel.x86_64 php54-php-mbstring.x86_64 php54-php-mcrypt.x86_64 php54-php-mysqlnd.x86_64
