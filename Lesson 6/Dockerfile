FROM ubuntu:18.04
RUN apt update
RUN apt install -y default-jdk
RUN apt install -y wget
RUN mkdir -m777 /home/tomcat
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.58/bin/apache-tomcat-9.0.58.tar.gz
RUN tar zxvf apache-tomcat-*.tar.gz -C /home/tomcat --strip-components 1
ADD FlyAway.war /home/tomcat/webapps/
EXPOSE 8080
CMD ["/home/tomcat/bin/catalina.sh", "run"]
