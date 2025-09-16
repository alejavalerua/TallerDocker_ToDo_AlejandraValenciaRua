FROM node:20-alpine AS base
WORKDIR /app

# Instala dependencias
COPY package*.json ./
RUN npm ci

# Copia código y compila
COPY . .
RUN npm run build

EXPOSE 3000
CMD ["node","/app/dist/index.js"]
