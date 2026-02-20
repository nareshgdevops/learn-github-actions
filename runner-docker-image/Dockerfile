FROM            docker.io/redhat/ubi9
RUN             curl -L -o /etc/yum.repos.d/hashi.repo https://rpm.releases.hashicorp.com/RHEL/hashicorp.repo
RUN             curl -L -o /etc/yum.repos.d/azure-cli.repo https://packages.microsoft.com/yumrepos/azure-cli
RUN             dnf install libicu make terraform azure-cli -y
RUN             useradd github
USER            github
WORKDIR         /home/github
RUN             curl -o actions-runner-linux-x64-2.331.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.331.0/actions-runner-linux-x64-2.331.0.tar.gz && tar xzf ./actions-runner-linux-x64-2.331.0.tar.gz
COPY            run.sh /
ENTRYPOINT      ["bash", "/run.sh"]
