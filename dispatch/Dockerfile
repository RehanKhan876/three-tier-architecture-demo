# Use a Go 1.19 image
FROM golang:1.19

# Set the working directory
WORKDIR /go/src/app

# Copy go.mod
COPY go.mod ./

# Download all dependencies
RUN go mod download

# Copy the rest of the code
COPY . .

# Build the Go application
RUN go build -o dispatch .

# Command to run the application
CMD ["./dispatch"]
