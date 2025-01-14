# Use the official Node.js image as a base image
FROM node:16

# Set working directory
WORKDIR /app

# Clean npm cache
RUN npm cache clean --force

# Install dependencies
COPY package*.json ./
RUN npm install

# Copy app files
COPY . .

# List contents of /app/src to debug
RUN ls -la /app/src

# Build the app
RUN npm run build

# Expose port and start the app
EXPOSE 3000
CMD ["npm", "start"]