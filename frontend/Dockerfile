# Use the official Node.js lts Alpine image as the base image
FROM node:16-alpine
# Set the working directory inside the container
WORKDIR /app

# add '/app/node_modules/.bin' to $PATH
ENV PATH /app/node_modules/.bin:$PATH

# install application dependencies
COPY package*.json ./

# Install application dependencies
RUN npm install

# copy app files
COPY . .

# Expose port 3000 to allow external access to the application
EXPOSE 3000

# Define the command to start the application
CMD ["npm", "start"]