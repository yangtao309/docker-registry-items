FROM shuyun/oracle-java8:latest

MAINTAINER YT <tao.yang@shuyun.com>

ENV JENKINS_SWARM_VERSION 1.22
ENV HOME /home/jenkins-slave

RUN apt-get update && apt-get install -y curl 

RUN useradd -c "Jenkins Slave user" -d $HOME -m jenkins-slave
RUN curl --create-dirs -sSLo /usr/share/jenkins/swarm-client-$JENKINS_SWARM_VERSION-jar-with-dependencies.jar http://maven.jenkins-ci.org/content/repositories/releases/org/jenkins-ci/plugins/swarm-client/$JENKINS_SWARM_VERSION/swarm-client-$JENKINS_SWARM_VERSION-jar-with-dependencies.jar \
  && chmod 755 /usr/share/jenkins

COPY jenkins-slave.sh /usr/local/bin/jenkins-slave.sh
RUN chmod 0755 /usr/local/bin/jenkins-slave.sh

USER jenkins-slave

VOLUME /home/jenkins-slave

ENTRYPOINT ["/usr/local/bin/jenkins-slave.sh"]

