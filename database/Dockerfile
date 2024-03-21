FROM mysql:latest
LABEL APP="studentapp"
LABEL maintainer="tejalpawar1819@gmail.com"
USER root
ENV MYSQL_ROOT_PASSWORD=1234
RUN mysql -u root -p1234 -e "create database studentapp";
RUN mysql -u root -p1234 -e "use studentapp";
RUN mysql -u root -p1234 studentapp -e "CREATE TABLE if not exists students(student_id INT NOT NULL AUTO_INCREMENT, student_name VARCHAR(100) NOT NULL, student_addr VARCHAR(100) NOT NULL, student_age VARCHAR(3) NOT NULL, student_qual VARCHAR(20) NOT NULL, student_percent VARCHAR(10) NOT NULL, student_year_passed VARCHAR(10) NOT NULL, PRIMARY KEY (student_id));"
RUN service mysql restart
EXPOSE 3306
