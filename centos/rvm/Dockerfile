FROM centos
MAINTAINER Viz <viz@linux.com>

# enable centos plus repo and install epel repo
RUN sed -i '0,/enabled=.*/{s/enabled=.*/enabled=1/}' /etc/yum.repos.d/CentOS-Base.repo
RUN yum install -y http://fedora.mirror.nexicom.net/epel/6/x86_64/epel-release-6-8.noarch.rpm
RUN yum update -y

# install necessary utilities
RUN yum install -y which tar

# install rvm
RUN curl -L get.rvm.io | bash -s stable
RUN source /etc/profile.d/rvm.sh
RUN /bin/bash -l -c "rvm requirements"
RUN /bin/bash -l -c "rvm install ruby"
RUN /bin/bash -l -c "gem install bundler --no-ri --no-rdoc"
