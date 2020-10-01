FROM jenkins/jenkins:lts
MAINTAINER denys naida <NaidaDV@nmu.one>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
COPY /home/ubuntu/dev_ip.txt /dev_ip.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER admin
ENV JENKINS_PASSWORD admin
