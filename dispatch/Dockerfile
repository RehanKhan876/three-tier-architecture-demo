# Use a Go version compatible with your application
FROM golang:1.19

# Set the working directory inside the container
WORKDIR /go/src/app

# Check if go.sum exists
RUN test -f go.sum || echo "go.sum does not exist, skipping copy"

# Copy go.mod and go.sum (if it exists)
COPY go.mod go.sum ./

# Download all dependencies
RUN go mod download

# Copy all the Go source files
COPY . .

# Initialize and tidy Go modules
RUN go mod init dispatch && go mod tidy

# Build the Go application
RUN go build -o dispatch .

# Command to run the application
CMD ["./dispatch"]
