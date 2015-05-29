FROM centos:centos7
RUN yum -y update
RUN yum -y install wget man git tig gcc make autoconf patch ntp curl-devel libyaml-devel libxml2-devel libxslt-devel

RUN yum install -y ibus-kkc vlgothic-*

# set locale
RUN yum reinstall -y glibc-common
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
