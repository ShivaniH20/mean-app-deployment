# Use a lightweight Node.js image
FROM node:18-alpine

# Set working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json first for caching
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy everything else (this includes server.js and app/)
COPY . .

# Expose port
EXPOSE 3000

# Start the backend
CMD ["node", "server.js"]
