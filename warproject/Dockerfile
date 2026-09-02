# Use an official Tomcat image with Java 17
FROM tomcat:10.1-jdk17-temurin

# Remove default Tomcat web applications to clean up space
RUN rm -rf /usr/local/tomcat/webapps/*

# Copy the .war file built by Maven from your target folder into Tomcat's webapps directory
# Tomcat automatically extracts and runs this war file as the root application
COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

# Expose port 8080 for web traffic
EXPOSE 8080

# Start Tomcat server
CMD ["catalina.sh", "run"]
