FROM ubuntu:20.04

RUN apt-get update \
    && apt-get install -y openssh-server \
    && apt-get install -y openjdk-11-jdk \
    && apt-get install -y curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Configuración del agente de Jenkins
ARG AGENT_WORKDIR=/home/jenkins/agent
RUN mkdir /home/jenkins \
    && useradd -d "$AGENT_WORKDIR" -u 1000 -m -s /bin/bash jenkins \
    && usermod -a -G users jenkins \
    && mkdir -p /usr/share/jenkins \
    && chown -R jenkins:jenkins /usr/share/jenkins \
    && mkdir -p /home/jenkins/.jenkins \
    && chown -R jenkins:jenkins /home/jenkins

# Descarga el JAR del agente de Jenkins
RUN curl -o /usr/share/jenkins/agent.jar https://url_del_agente/agent.jar

USER jenkins
ENV AGENT_WORKDIR=${AGENT_WORKDIR}
VOLUME /home/jenkins/.jenkins
WORKDIR /home/jenkins/agent

CMD ["/usr/sbin/sshd", "-D"]
