# Use a specific version of golang as base image
FROM golang:1.16

# Expose port 8080
EXPOSE 8080

# Set working directory
WORKDIR /usr/src/app

# Copy the application code
COPY . .

# Run installer
RUN go build

#Execute the file
CMD ["./server"]
