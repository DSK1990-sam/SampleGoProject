# Start from the latest golang base image
FROM golang:latest

# Set the Current Working Directory inside the container
WORKDIR /test

#to get mod and sum files
RUN go mod init sampleproject1

# copying server.go into app which is working directory
COPY server.go .

# Download all dependencies. Dependencies will be cached if the go.mod and go.sum files are not changed
RUN go mod download


# Build the Go app
RUN go build -o main .

# Expose port 9091 to the outside world
EXPOSE 8080

# Command to run the executable
CMD ["./main"]

