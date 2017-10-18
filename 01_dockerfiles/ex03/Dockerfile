# docker build -t go .
# docker run -p 3000:3000 -it go
# follow the installation steps and then try git clone through http and ssh

FROM            golang

LABEL           maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

RUN             apt-get update -y && apt-get upgrade -y \
                && mkdir -p $GOPATH/src/github.com/gogits \
                && cd $GOPATH/src/github.com/gogits \
                && git clone --depth=1 -b develop https://github.com/gogits/gogs \
                && cd gogs \
                && go build -tags "sqlite"

EXPOSE          3000

WORKDIR         $GOPATH/src/github.com/gogits/gogs

ENV             USER=root

CMD             su root -c "./gogs web"
