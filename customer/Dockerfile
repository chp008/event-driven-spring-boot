FROM openjdk:8-jdk-alpine
MAINTAINER michael.ploed@innoq.com
VOLUME /tmp
ADD target/customer-0.0.1-SNAPSHOT.jar app.jar
ENV JAVA_OPTS=""
ENV SPRING_APPLICATION_JSON='{"routeToSelf": "http://customer:9002/", "spring": {"rabbitmq": {"host": "localrabbit", "addresses": "rabbit-mq"}}}'
ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar /app.jar
EXPOSE 9002