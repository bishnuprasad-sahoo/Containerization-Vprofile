FROM maven AS BUILD_IMAGE
RUN git clone https://github.com/hkhcoder/vprofile-project.git
RUN cd vprofile-project && git checkout containers && mvn install

FROM tomcat
# Good Prcatice to maintain tags/LABEL
LABEL "Project"="Vprofile"
LABEL "Author"="Bishnu"

RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=BUILD_IMAGE target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]