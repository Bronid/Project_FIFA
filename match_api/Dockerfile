# Use an official Node.js runtime as a base image
FROM node:16

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy only package.json and package-lock.json to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the application code into the container
COPY . .

# Expose the port your app runs on
EXPOSE 8080

# Command to run your application
CMD ["node", "app.mjs"]


