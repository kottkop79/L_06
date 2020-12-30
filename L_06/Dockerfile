FROM tomcat:9
RUN apt-get update
RUN apt-get install default-jdk -y
RUN apt-get install git -y
RUN apt-get install maven -y
RUN rm -rf /usr/local/tomcat/webapps/*
RUN mkdir kopf_ /home/kopf_
WORKDIR /home/kopf_
RUN cd /home/kopf_
RUN git clone https://github.com/koddas/war-web-project.git
WORKDIR /home/kopf_/war-web-project/
RUN cd /home/kopf_/war-web-project/
RUN mvn package
RUN cp -a /home/kopf_/war-web-project/target/wwp-1.0.0.war /usr/local/tomcat/webapps/
