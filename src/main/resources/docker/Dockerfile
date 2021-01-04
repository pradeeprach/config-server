FROM alpine

WORKDIR /home/config-server

RUN apk add build-base \
    && apk update \
    && apk upgrade \
    && apk add bash \
    && apk add curl \
    && apk add openjdk11 --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community

ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk
ENV PATH=$JAVA_HOME/bin:$PATH

ADD config-server-0.0.1-SNAPSHOT.jar /home/config-server

EXPOSE 9999

ENTRYPOINT ["java","-jar","/home/config-server/config-server-0.0.1-SNAPSHOT.jar"]