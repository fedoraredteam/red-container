FROM fedora
LABEL maintainer="security@lists.fedoraproject.org"

RUN dnf upgrade -y && \
    dnf install -y \
      findutils \
      nmap && \
    useradd -c 'Metasploit Framework' -m -s /sbin/nologin metasploit
RUN curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb | sh
USER metasploit
CMD ["msfconsole", "-v"]
