FROM zurelian/java.base

MAINTAINER Bohdan Levchenko, bohdan-levchenko.com

ENV TOMCAT_VERSION 8.5.15
ENV APP_NAME apache-tomcat-${TOMCAT_VERSION}
ENV INSTALL_DIR /opt
ENV SERVER_HOME ${INSTALL_DIR}/${APP_NAME}
RUN curl -o ${SERVER_HOME}.zip -L http://apache.volia.net/tomcat/tomcat-8/v${TOMCAT_VERSION}/bin/${APP_NAME}.zip
RUN unzip ${SERVER_HOME}.zip -d ${INSTALL_DIR}
RUN chmod +x ${SERVER_HOME}/bin/catalina.sh
ENV DEPLOYMENT_DIR ${SERVER_HOME}/webapps/
ENTRYPOINT ${SERVER_HOME}/bin/catalina.sh run
EXPOSE 8080
