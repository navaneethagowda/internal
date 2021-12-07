FROM centos:latest
RUN yum install java -y
RUN mkdir /app/tomcat
WORKDIR /app/tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.55/bin/apache-tomcat-9.0.55.tar.gz .
RUN tar -xvz apache-tomcat-9.0.55.tar.gz
RUN mv apache-tomcat-9.0.55/* /app/tomcat
EXPOSE 8080
CMD ["/app/tomcat/bin/catalina.sh", "run"]
