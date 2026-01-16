FROM tomcat:7-jre8

COPY drop/* /usr/local/tomcat/webapps/

#EXPOSE 8080
EXPOSE 8082

#ENTRYPOINT ["catalina.sh", "run"]
ENTRYPOINT ["/bin/sh", "-c", "P=8082; sed \"s/8080/$P/g\" < conf/server.xml > /tmp/srv.xml && catalina.sh run -config /tmp/srv.xml"]