FROM node:14-alpine3.12

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json first
COPY backend/package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY backend/ ./

# Expose the required port
EXPOSE 4000

# Command to run the application
CMD ["node", "index.js"]
