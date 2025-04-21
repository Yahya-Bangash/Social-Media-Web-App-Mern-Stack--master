FROM node:16-alpine
# Set working directory
WORKDIR /app
# Copy package.json and package-lock.json
COPY package*.json ./
# Install dependencies
RUN npm install
# Copy the rest of the application
COPY . .
# Create a directory for uploaded images if it doesn't exist
RUN mkdir -p images
# Expose the port
EXPOSE 4000
# Start the application
CMD ["npm", "start"] 