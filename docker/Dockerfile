FROM jboss/wildfly


RUN /opt/jboss/wildfly/bin/add-user.sh admin Admin#70365 --silent
COPY wildfly-spring-boot-sample-1.0.0.war /opt/wildfly/standalone/deployments/
EXPOSE 8080 9990 9090
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-c", "standalone-full.xml", "-b", "0.0.0.0"]
