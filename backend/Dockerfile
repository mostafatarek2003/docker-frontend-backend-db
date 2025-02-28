# Use the official Node.js lts Alpine image as the base image
FROM node:lts-alpine3.21

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install the dependencies defined in package.json
RUN npm install

# Copy the rest of the application files into the container
COPY . .

# Expose port 3001 to allow external access to the application
EXPOSE 3001

# Define the command to run the application
CMD ["node", "server.js"]
