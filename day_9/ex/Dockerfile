# Use an official base image
FROM node:14

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed dependencies
RUN npm install

# Expose port 3000 to the outside world
EXPOSE 3000

# Run node when the container launches
CMD ["node", "index.js"]
