# Name:     store-cloud-web-search
# Time:     2017-05-07

FROM java:8-jre-alpine

MAINTAINER Binux <xu.binux@gmail.com>

RUN mkdir /app

WORKDIR /app

COPY store-cloud-web-search-1.0.0.jar /app

ADD http://on2bs9q7q.bkt.clouddn.com/wait-for-it.sh /

RUN chmod +x /wait-for-it.sh

ENTRYPOINT ["./wait-for-it.sh", "store-cloud-service-search:8512","--", "java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "/app/store-cloud-web-search-1.0.0.jar"]

EXPOSE 8102