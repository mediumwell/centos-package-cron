FROM centos:7.0.1406
MAINTAINER Brady Wied <brady@bswtechconsulting.com>
RUN yum -y --disablerepo=updates install python-setuptools git epel-release yum-utils
RUN yum -y --disablerepo=updates install python-pip mailx python-sqlalchemy sudo
# Newer versions of mock need setuptools > 17.0
RUN pip install --upgrade pip && pip install setuptools --upgrade
RUN useradd -m nonrootuser -G wheel
RUN echo "nonrootuser ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
