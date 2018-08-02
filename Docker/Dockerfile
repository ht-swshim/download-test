FROM anapsix/alpine-java:8_jdk
MAINTAINER Seongwon Shim <swshim@hdtel.co.kr>

ENV TZ=Asia/Seoul
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN mkdir /webapps
COPY target/file_download_core_framework-0.0.1-SNAPSHOT.jar /webapps/download-test.jar

ENTRYPOINT java -Xmx2048m -Xss512k -jar /webapps/download-test.jar && bash

