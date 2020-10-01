FROM jenkins/jenkins:lts
MAINTAINER denys naida <NaidaDV@nmu.one>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
COPY dev_ip.txt /usr/share/jenkins/dev_ip.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER admin
ENV JENKINS_PASSWORD admin
ENV DEV_IP_JEN=$(`cat /tmp/final_task/dev_ip.txt`)
ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/jenkins.sh"]
