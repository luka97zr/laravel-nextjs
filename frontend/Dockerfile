FROM node:20.1.0-alpine

# Set the working directory to /app
WORKDIR /var/www/html

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the current directory contents into the container at /app
COPY . .

# Build the Next.js app
RUN npm build

# Expose port 3000
EXPOSE 3000

# Command to run the application
CMD ["npm", "start"]