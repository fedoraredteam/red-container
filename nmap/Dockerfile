FROM fedora
LABEL maintainer="security@lists.fedoraproject.org"

ENV NMAP_PRIVILEGED=""

RUN dnf upgrade -y && dnf install -y nmap

ENTRYPOINT ["nmap"]
CMD ["--version"]
