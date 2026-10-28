FROM tomcat:11.0-jdk17
RUN rm -rf /usr/local/tomcat/webapps/* \
 && groupadd -r pc-app && useradd -r -g pc-app pc-app \
 && chown -R pc-app:pc-app /usr/local/tomcat
COPY target/petclinic.war /usr/local/tomcat/webapps/ROOT.war
USER pc-app
EXPOSE 8080
