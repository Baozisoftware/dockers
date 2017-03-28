#Base image
FROM ubuntu:16.04
MAINTAINER Baozisoftware Diklic "https://github.com/Baozisoftware"

#Download luzhibo
ADD https://github.com/Baozisoftware/luzhibo/releases/download/latest/luzhibo_linux_amd64 /
RUN chmod +x luzhibo

#Other
EXPOSE 12216
CMD /luzhibo