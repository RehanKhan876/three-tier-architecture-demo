FROM golang:1.19

WORKDIR /go/src/app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

RUN go mod init dispatch && go mod tidy

RUN go build -o dispatch .

CMD ["./dispatch"]
