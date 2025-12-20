# Use official Node LTS image
FROM node:20-alpine

# Set working directory
WORKDIR /server

# Copy package files first (better caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the source code
COPY . .

# Expose backend port
EXPOSE 8000

# Start server
CMD ["npm", "run", "dev"]
