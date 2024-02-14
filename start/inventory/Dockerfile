FROM icr.io/appcafe/open-liberty:kernel-slim-java11-openj9-ubi
WORKDIR /config
COPY --chown=1001:0 src/main/liberty/config /config
RUN features.sh
COPY --chown=1001:0 /config/*.jar app.jar
RUN configure.sh
