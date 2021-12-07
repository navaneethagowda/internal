FROM centos:latest
RUN yum install java -y
RUN mkdir -p /opt/tomcat
WORKDIR /opt/tomcat
COPY apache-tomcat-9.0.55.tar.gz .
RUN tar -xvzf apache-tomcat-9.0.55.tar.gz
RUN mv apache-tomcat-9.0.55/* /opt/tomcat
COPY MyMavenApp.war /opt/tomcat/webapps
EXPOSE 8080
CMD ["/opt/tomcat/bin/catalina.sh", "run"]
