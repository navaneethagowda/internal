FROM centos:latest
RUN yum install java -y
RUN mkdir -p /opt/tomcat
WORKDIR /opt/tomcat
#ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.55/bin/apache-tomcat-9.0.55.tar.gz .
COPY apache-tomcat-9.0.56.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.56.tar.gz
RUN mv apache-tomcat-9.0.56/* /opt/tomcat
COPY MyMavenApp.war /opt/tomcat/webapps
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
