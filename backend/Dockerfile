FROM centos:7

LABEL APP="Studentapp"
USER root
WORKDIR /opt/
ADD https://downloads.apache.org/tomcat/tomcat-9/v9.0.96/bin/apache-tomcat-9.0.96-fulldocs.tar.gz.sha512
RUN tar -xzvf apache-tomcat-8.5.99.tar.gz 
RUN yum install java -y
WORKDIR /opt/apache-tomcat-8.5.99
COPY student.war  webapps/student.war
COPY context.xml conf/context.xml
ADD mysql-connector.jar lib/mysql-connector.jar

EXPOSE 8080

CMD ["bin/catalina.sh" , "run"]
