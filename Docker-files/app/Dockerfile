FROM maven:3.9.9-eclipse-temurin-21-janny
RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat:10-jdk21
RUN rm -rf /user/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapp/ROOT.war

EXPOSE 8080
CMD [ "catalina.sh", "run" ]