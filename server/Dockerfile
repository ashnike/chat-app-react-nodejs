# Stage 1: Build the backend application
FROM node:18-alpine AS builder
# Set the working directory
WORKDIR /app
COPY package*.json ./

RUN npm install
COPY . .
FROM node:18-alpine

# Set the working directory
WORKDIR /app
COPY --from=builder /app .
EXPOSE 5000

# Start the application
CMD ["node", "index.js"]
