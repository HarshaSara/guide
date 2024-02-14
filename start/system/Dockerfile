FROM icr.io/appcafe/open-liberty:kernel-slim-java11-openj9-ubi

COPY --chown=1001:0 src/main/liberty/config /config
RUN features.sh
RUN mvn -f /config/pom.xml clean package
COPY --chown=1001:0 /config/*.jar app.jar
RUN configure.sh
