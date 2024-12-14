# Use the official Node.js image.
FROM node:14

# Set the working directory.
WORKDIR /usr/src/app

# Copy package.json and package-lock.json.
COPY package*.json ./

# Install dependencies.
RUN npm install

# Copy the rest of the application files.
COPY . .

# Build the React app.
RUN npm run build

# Use a lightweight web server to serve the React app.
RUN npm install -g serve
CMD ["serve", "-s", "build"]

# Expose the frontend port.
EXPOSE 3000
