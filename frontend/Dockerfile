FROM node:16 AS build

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

CMD ["npx", "-y", "serve", "-s", "build", "-l", "8000"]