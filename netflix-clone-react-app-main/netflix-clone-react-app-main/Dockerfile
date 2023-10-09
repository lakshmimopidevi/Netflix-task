# Use an official Node.js runtime as the base image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install application dependencies
RUN yarn install

# Copy the rest of the application code to the container
COPY . .

# Build the React application
RUN yarn build

# Expose port 80 for the application
EXPOSE 80

# Start the application when the container is run
CMD ["yarn", "start"]
