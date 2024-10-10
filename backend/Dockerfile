# Stage 1: Build frontend
FROM node:14-alpine AS builder
WORKDIR /app
COPY ./frontend/package*.json ./
RUN npm install
COPY ./frontend ./
RUN npm run build

# Stage 2: Build backend
FROM node:14-alpine
WORKDIR /app
COPY ./backend/package*.json ./
RUN npm install
COPY ./backend ./
COPY --from=builder /app/build ./build

# Serve the app
CMD ["node", "index.js"]
