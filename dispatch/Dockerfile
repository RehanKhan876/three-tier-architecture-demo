# Use a Go 1.19 image
FROM golang:1.17

WORKDIR /go/src/app

COPY *.go .

RUN go mod init dispatch && go get
RUN go install
