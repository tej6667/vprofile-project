FROM maven:3.9.9-eclipse-temurin-21-jammy AS mvn_container
LABEL "Project"="vprofile"
LABEL "Author"="TT"
RUN git clone https://github.com/tej6667/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install
#RUN mvn clean



FROM tomcat:10-jdk21
LABEL "Project"="vprofile"
LABEL "Author"="TT"
RUN rm -rf /usr/local/tomcat/webapps/*

COPY --from=mvn_container /vprofile-project/target/vprofile.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]

