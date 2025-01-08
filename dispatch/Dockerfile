FROM golang:1.19

WORKDIR /go/src/app

COPY *.go .

RUN go mod init dispatch && go mod tidy
RUN go build -o dispatch .

CMD ./dispatch
