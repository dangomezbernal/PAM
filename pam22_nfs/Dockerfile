# pam

FROM debian:latest
LABEL author="@dan ASIX-M06"
LABEL subject="ldapserver 2022"
RUN apt-get update
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get -y install procps iproute2 tree nmap vim less finger passwd libpam-pwquality libpam-mount nfs-common
RUN mkdir /opt/docker
WORKDIR /opt/docker
COPY * /opt/docker/
COPY common-session /etc/pam.d/
COPY pam_mount.conf.xml /etc/security
RUN chmod +x /opt/docker/startup.sh
CMD /opt/docker/startup.sh

