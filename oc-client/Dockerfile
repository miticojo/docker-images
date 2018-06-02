FROM centos:centos7
LABEL maintainer="miticojo@gmail.com"

RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-$(rpm -E '%{rhel}').noarch.rpm && \
    yum install -y jq && yum clean all && rm -rf /var/cache/yum

RUN curl -L `curl -s https://api.github.com/repos/openshift/origin/releases/latest | jq -r ".assets[] | select(.browser_download_url | contains(\"linux\")) | select(.browser_download_url | contains(\"server\") | not ) | .browser_download_url"` | tar xz -C /tmp

RUN find /tmp -name oc -type f -exec mv {} /usr/sbin/oc \;
