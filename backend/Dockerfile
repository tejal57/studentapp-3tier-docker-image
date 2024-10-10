FROM centos:7

LABEL APP="Studentapp"
USER root
WORKDIR /opt/
RUN curl -O https://downloads.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96.tar.gz
RUN tar -xzvf apache-tomcat-9.0.96.tar.gz 
RUN apt install default-jdk -y
WORKDIR /opt/apache-tomcat-9.0.96
COPY student.war  webapps/student.war
COPY context.xml conf/context.xml
ADD mysql-connector.jar lib/mysql-connector.jar

EXPOSE 8080

CMD ["bin/catalina.sh" , "run"]
