FROM maven AS mvn_container
LABEL "Project"="vprofile"
LABEL "Author"="TT"
RUN git clone --branch ttcontainers https://github.com/tej6667/vprofile-project.git && cd vprofile-project && mvn install


FROM tomcat
LABEL "Project"="vprofile"
LABEL "Author"="TT"
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=mvn_container /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war
EXPOSE 8080
CMD ["catalina.sh", "run"]

