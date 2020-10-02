FROM jenkins/jenkins:lts
MAINTAINER denys naida <NaidaDV@nmu.one>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER=admin
ENV JENKINS_PASS=admin
ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/jenkins.sh"]
