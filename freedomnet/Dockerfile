#Base image
FROM ubuntu:16.04
MAINTAINER Baozisoftware "https://github.com/Baozisoftware"

ENV V2VERSION 4.25.1
ENV V2PORT 80
ENV V2GUID 214385d0-82ca-4a12-a7b9-eb3229ceb890
ENV V2PATH b54f

#Install V2ray
ADD https://github.com/v2ray/v2ray-core/releases/download/v$V2VERSION/v2ray-linux-64.zip /
RUN apt update
RUN apt install unzip
RUN unzip v2ray-linux-64.zip

#Setup V2ray
COPY config.json /config.json
RUN sed -i "s/_port_/$V2PORT/g" /config.json
RUN sed -i "s/_guid_/$V2GUID/g" /config.json
RUN sed -i "s/_path_/$V2PATH/g" /config.json

#Start
EXPOSE $V2PORT
CMD ["/v2ray","-config","/config.json"]
