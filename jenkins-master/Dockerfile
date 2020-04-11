FROM jenkins/jenkins:lts
LABEL maintainer="lain@navi"

# Create jenkins log dir
USER root
RUN mkdir /var/log/jenkins
RUN mkdir /var/cache/jenkins
RUN chown -R jenkins:jenkins /var/log/jenkins
RUN chown -R jenkins:jenkins /var/cache/jenkins
USER jenkins

ENV JAVA_OPTS="-Xmx512m"
ENV JENKINS_OPTS=" --handlerCountMax=10 --logfile=/var/log/jenkins/jenkins.log --webroot=/var/cache/jenkins/war"


