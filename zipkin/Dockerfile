FROM openjdk:8-jre-alpine

EXPOSE 9411

RUN wget -O zipkin.jar 'https://search.maven.org/remote_content?g=io.zipkin.java&a=zipkin-server&v=LATEST&c=exec'
RUN chown -R 1001:0 zipkin.jar
USER 1001

ENTRYPOINT ["java", "-jar", "zipkin.jar"]
