# Use a specific version of Node.js as base image
FROM node:14

# Expose port 5000
EXPOSE 5000

# Set working directory
WORKDIR /usr/src/app

# Copy the application code
COPY . .

# Install dependencies
RUN npm install 

# Add ENV with the necessary information
ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Build the static files
RUN npm run build

# Use npm package called serve to serve the project in port 5000
RUN npm install -g serve
CMD ["serve", "-s", "-l", "5000", "build"]
