# Use the official Node.js LTS image
FROM node:18

# Set the working directory
WORKDIR /app

# Copy only package.json and package-lock.json first (for better caching)
COPY package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of your backend code
COPY . .

# Expose the backend port (change if your app uses a different one)
EXPOSE 5000

# Start the backend using node (not nodemon in production)
CMD ["node", "server.js"]

