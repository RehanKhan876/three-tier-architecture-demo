# Use the official Go 1.21 image as the base image
FROM golang:1.22

# Set the working directory inside the container
WORKDIR /go/src/app

# Copy all Go source files into the container's working directory
COPY *.go .

# Initialize a new Go module (if not already initialized)
RUN go mod init dispatch || true

# Download and tidy up the Go module dependencies
RUN go mod tidy

# Build the Go application and create an executable named "dispatch"
RUN go build -o dispatch .

# Set the default command to run the application
CMD ["./dispatch"]
