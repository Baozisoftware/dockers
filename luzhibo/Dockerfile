#Base image
FROM ubuntu:16.04
MAINTAINER Baozisoftware Diklic "https://github.com/Baozisoftware"

#Install FFmpeg
RUN apt-get update
RUN apt-get -y ffmpeg

#Download luzhibo
ADD https://github.com/Baozisoftware/luzhibo/releases/download/latest/luzhibo_linux_amd64 /
RUN chmod +x luzhibo_linux_amd64

#Other
EXPOSE 12216
CMD /luzhibo_linux_amd64
