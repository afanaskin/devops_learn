FROM ubuntu:18.04
RUN apt update && apt install -y \
default-jdk \
git \
maven \
wget \
&& rm -rf /var/lib/apt/lists/* \
&& mkdir -m777 /home/tomcat /home/git \
&& wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.58/bin/apache-tomcat-9.0.58.tar.gz \
&& tar zxvf apache-tomcat-*.tar.gz -C /home/tomcat --strip-components 1 \
&& git clone https://github.com/deepshankaryadav/CyberFRAT-DevSecOps-Training-Sample-Java-App.git /home/git \
&& cd /home/git \
&& mvn package \
&& cp /home/git/target/WebApp.war /home/tomcat/webapps/
EXPOSE 8080
CMD ["/home/tomcat/bin/catalina.sh", "run"]
