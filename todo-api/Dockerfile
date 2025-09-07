# Use a small, modern Node image
FROM node:20-alpine

# Work dir in the container
WORKDIR /app

# Install deps first (better layer caching)
COPY package*.json ./
# ci = clean reproducible install, faster & safer for CI
RUN npm ci

# Copy the rest of the source
COPY . .

# Build TypeScript -> dist/
RUN npm run build

# Expose the port your server uses
EXPOSE 5000

# Run the compiled server (production, no nodemon)
CMD ["node", "dist/index.js"]
