from ubuntu:14.04
MAINTAINER SaltStack, Inc.

RUN apt-get update && \
    apt-get -y install wget curl -o DPkg::Options::=--force-confold && \
    wget -O - https://repo.saltstack.com/apt/ubuntu/14.04/amd64/latest/SALTSTACK-GPG-KEY.pub | apt-key add - && \
    echo "deb http://repo.saltstack.com/apt/ubuntu/14.04/amd64/latest trusty main" > /etc/apt/sources.list.d/saltstack.list && \
    apt-get update && \
    apt-get -y install openssh-server salt-master salt-minion -o DPkg::Options::=--force-confold && \
    curl --silent -L https://www.getchef.com/chef/install.sh | sh
