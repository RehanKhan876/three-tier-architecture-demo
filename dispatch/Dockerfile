FROM golang:1.19

# Set the working directory inside the container
WORKDIR /go/src/app

# Copy the Go module files first (to leverage Docker caching)
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
