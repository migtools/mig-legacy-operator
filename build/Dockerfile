FROM quay.io/operator-framework/ansible-operator:latest

USER root

RUN yum -y update && yum clean all

RUN echo -ne "[centos-8-appstream]\nname = CentOS 8 (RPMs) - AppStream\nbaseurl = http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/\nenabled = 1\ngpgcheck = 0" > /etc/yum.repos.d/centos.repo

RUN yum -y install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm \
 && yum -y install python3-boto3 nss_wrapper \
 && yum clean all

RUN ln -s ${HOME}/.ansible /.ansible
COPY build/entrypoint /usr/local/bin/entrypoint
COPY deploy/operator.yml /operator.yml
COPY deploy/controller.yml /controller.yml
USER 1001

RUN ansible-galaxy collection install operator_sdk.util community.kubernetes
RUN  chmod -R ug+rwx ${HOME}/.ansible

COPY watches.yaml ${HOME}/watches.yaml

COPY roles/ ${HOME}/roles/
ENTRYPOINT /usr/local/bin/entrypoint
