FROM rockylinux:9.3
LABEL MAINTAINER="Danylo Mikula <dan@mikula.dev>"

ENV USER=root
ENV LOGNAME=root

RUN dnf -y upgrade && \
    dnf -y install epel-release dnf-plugins-core && \
    dnf -y install wget procps gcc make perl bzip2 dkms kernel-devel kernel-headers && \
    dnf config-manager --add-repo=https://download.virtualbox.org/virtualbox/rpm/el/virtualbox.repo && \
    dnf config-manager --add-repo=https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo && \
    dnf -y install VirtualBox-7.0 vagrant && \
    dnf clean all && \
    rm -rf /var/cache/dnf /var/tmp/* /tmp/*

CMD ["bash"]
