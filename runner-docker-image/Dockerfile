FROM            docker.io/redhat/ubi9
RUN             useradd github
USER            github
WORKDIR         /home/github
RUN             curl -o actions-runner-osx-x64-2.331.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.331.0/actions-runner-osx-x64-2.331.0.tar.gz &&tar xzf ./actions-runner-osx-x64-2.331.0.tar.gz
