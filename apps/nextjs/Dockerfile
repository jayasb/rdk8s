FROM node:18-alpine

WORKDIR /app

# Install create-next-app globally
RUN npm install -g create-next-app@latest

# Create Next.js app with specific configurations
RUN npx create-next-app@latest . \
    --typescript \
    --tailwind \
    --eslint \
    --app \
    --src-dir false \
    --import-alias "@/*" \
    --no-git \
    --yes

# Dynamically create next.config.js
RUN echo "module.exports = { basePath: process.env.BASE_PATH || '' };" > next.config.js

# Install dependencies
RUN npm install

# Build the application
ARG BASE_PATH
ENV BASE_PATH=${BASE_PATH}
RUN npm run build

EXPOSE 3000

# Start the application
CMD ["npm", "start"]