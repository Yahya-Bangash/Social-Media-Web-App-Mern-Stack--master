FROM node:16-alpine
WORKDIR /app
# Copy package.json and package-lock.json
COPY package*.json ./
# Install dependencies
RUN npm install
# Copy the rest of the application
COPY . .
# Build the application
RUN npm run build
# Install a simple server to serve the static content
RUN npm install -g serve
# Expose the port
EXPOSE 3000
# Start the application
CMD ["serve", "-s", "build", "-l", "3000"] 