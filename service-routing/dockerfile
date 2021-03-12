FROM adoptopenjdk:11-jre-hotspot-bionic

COPY graphhopper-web-2.3.jar graphhopper-web-2.3.jar

ENTRYPOINT [ "java", "-jar", "./graphhopper-web-2.3.jar" ]
CMD [ "check", "conf/config.yml" ]
