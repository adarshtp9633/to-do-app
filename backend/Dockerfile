FROM node:14-alpine3.12

# Set the working directory inside the container
WORKDIR /app

# Copy the contents of the backend folder to the working directory
COPY backend/ ./

# Expose the required port
EXPOSE 4000

# Command to run the application
CMD ["node", "index.js"]

