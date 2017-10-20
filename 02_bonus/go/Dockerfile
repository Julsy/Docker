# to run: docker build -t go .
# docker run -it --rm go
# vi hello.go
# package main
#  import "fmt"
#  func main() {
#     fmt.Println("hello world")
#  }
# go run hello.go

FROM    ubuntu
LABEL   maintainer="Iuliia Iliuk iiliuk@student.42.us.org"

RUN     mkdir -p /goroot && \
        apt-get update && \
        apt-get -y upgrade && \
        apt-get install -y build-essential && \
        apt-get install -y vim && \
        apt-get install -y curl && \
        curl https://storage.googleapis.com/golang/go1.4.2.linux-amd64.tar.gz | tar xvzf - -C /goroot --strip-components=1

ENV     GOROOT /goroot
ENV     GOPATH /gopath
ENV     PATH $GOROOT/bin:$GOPATH/bin:$PATH

WORKDIR /gopath

CMD     ["bash"]
