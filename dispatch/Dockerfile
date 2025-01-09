FROM golang:1.17

WORKDIR /go/src/app

# Copy the Go source files
COPY *.go .

# Initialize the Go module (if not already initialized)
RUN go mod init dispatch || true

# Download dependencies
RUN go mod tidy

# Build the Go application
RUN go build -o dispatch .

# Set the entrypoint
CMD ["./dispatch"]
