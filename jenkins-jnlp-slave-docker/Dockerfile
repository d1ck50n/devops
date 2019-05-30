# This file originated from https://github.com/jenkinsci/docker-jnlp-slave/blob/master/Dockerfile

FROM jenkins/slave:latest
LABEL Description="Jenkins JNLP agents, contains kubectl and Docker"

USER root

RUN wget https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl && \
    chmod +x ./kubectl && \
    mv ./kubectl /usr/local/bin/kubectl

RUN curl -fsSL https://get.docker.com -o get-docker.sh && \
  sh get-docker.sh

COPY jenkins-slave /usr/local/bin/jenkins-slave
RUN chmod +x  /usr/local/bin/jenkins-slave

ENTRYPOINT ["jenkins-slave"]