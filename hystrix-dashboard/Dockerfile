#
# Creates a docker container with a running Hystrix Web App
#

FROM centos:6

MAINTAINER Marcel Birkner <marcel.birkner@codecentric.de>

RUN yum -y install java-1.8.0-openjdk

ENV HYSTRIX_VERSION 1.4.12
ENV JETTY_VERSION 9.3.0.v20150612

ENV MAVEN_REPO_HYSTRIX https://repo1.maven.org/maven2/com/netflix/hystrix/hystrix-dashboard
ENV MAVEN_REPO_JETTY https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-runner

WORKDIR /app

RUN curl $MAVEN_REPO_HYSTRIX/$HYSTRIX_VERSION/hystrix-dashboard-$HYSTRIX_VERSION.war -o hystrix-dashboard.war

RUN curl $MAVEN_REPO_JETTY/$JETTY_VERSION/jetty-runner-$JETTY_VERSION.jar -o jetty-runner.jar

EXPOSE 8080

CMD [ "java", "-cp", "jetty-runner.jar", "org.eclipse.jetty.runner.Runner", "hystrix-dashboard.war" ]
