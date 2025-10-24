# Use a modern Node.js base image (Vue CLI supports Node 16+; 18 is stable LTS)
FROM mcr.microsoft.com/vscode/devcontainers/javascript-node:18

# Install Vue CLI globally
RUN npm install -g @vue/cli @vue/cli-service-global http-server

# Set working directory
WORKDIR /workspaces/vscode-dev-container-vue

# Copy dependency files first for better caching
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the rest of the source code
COPY . .

# Expose Vue CLI default dev server port
EXPOSE 8080

# Run Vue CLI service in development mode
CMD ["npm", "run", "serve"]
