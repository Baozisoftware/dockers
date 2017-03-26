#Base image
FROM ubuntu:16.04
MAINTAINER Baozisoftware Diklic "https://github.com/Baozisoftware"

#Install git,golang
RUN apt-get update
RUN apt-get install git golang
ENV GOPATH ~/go

#Build Luzhibo
RUN go get github.com/josephspurrier/goversioninfo/cmd/goversioninfo
RUN go get github.com/PuerkitoBio/goquery
RUN go get github.com/pkg/browser
RUN go get github.com/Baozisoftware/qrcode-terminal-go
RUN git clone https://github.com/Baozisoftware/Luzhibo-go.git $GOPATH\src\luzhibo

#Other
EXPOSE 12216
CMD $GOPATH\src\luzhibo\luzhibo