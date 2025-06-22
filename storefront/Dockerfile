FROM node:18-alpine

WORKDIR /app

# Copy package files
COPY package.json pnpm-lock.yaml ./

# Install pnpm and dependencies
RUN npm install -g pnpm
RUN pnpm install

# Copy source code
COPY . .

# Set environment variables for runtime (not build)
ENV NODE_ENV=development
ENV NEXT_TELEMETRY_DISABLED=1
ENV SKIP_PUBLISHABLE_KEY_CHECK=true

# Expose port
EXPOSE 3000

# Start the application in development mode
CMD ["pnpm", "dev"]