#Base image
FROM ubuntu:16.04
MAINTAINER Baozisoftware Diklic "https://github.com/Baozisoftware"

#Install Luzhibo
ADD https://github.com/Baozisoftware/Luzhibo-go/releases/download/latest/releases.7z 
RUN apt-get update
RUN apt-get install p7zip
RUN 7z releases.7z
RUN chmod +x luzhibo_linux_amd64

#Other
EXPOSE 12216
CMD /luzhibo_linux_amd64