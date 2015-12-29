# Use latest jboss/wildfly image as the base 
# https://hub.docker.com/r/jboss/wildfly/
FROM jboss/wildfly

# Add a user in administration realm
RUN /opt/jboss/wildfly/bin/add-user.sh admin Admin#007 --silent

# Set the default command to run on boot
# This will boot JBoss  in the standalone mode and bind to all interface
CMD ["/opt/jboss/wildfly/bin/standalone.sh", "-b", "0.0.0.0" , "-bmanagement", "0.0.0.0"]
