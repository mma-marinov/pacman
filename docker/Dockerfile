FROM node:jod

MAINTAINER Ivan Font <ifont@redhat.com>

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Clone game source code
RUN git clone https://github.com/mma-marinov/pacman.git .

# Install app dependencies
RUN npm install
# Install the @splunk/otel package
RUN npm install @splunk/otel
# Set appropriate permissions
RUN chmod -R go+r /node_modules/@splunk/otel

# Expose port 8080
EXPOSE 8080

# Run container
CMD ["npm", "start"]
