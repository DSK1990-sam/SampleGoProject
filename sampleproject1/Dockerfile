# Start from the latest golang base image
FROM golang:latest

# Set the Current Working Directory inside the container
WORKDIR /test

# copying server.go into app which is working directory
COPY server.go .


# Build the Go app
RUN go build -o test .

# Expose port 8080 to the outside world
EXPOSE 8080

# Command to run the executable
CMD ["./test"]R
