# frontend/Dockerfile
FROM node:14

WORKDIR /app

COPY package.json ./
RUN npm install

COPY . .

RUN npm run build

# Serve the build files using a simple static server
RUN npm install -g serve
CMD ["serve", "-s", "build"]
