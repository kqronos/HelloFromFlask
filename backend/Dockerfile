# frontend/Dockerfile
FROM node:20-alpine as build
WORKDIR /app
COPY package*.json ./
RUN apt-get update && apt-get install -y nodejs npm
RUN npm install
COPY . .
RUN npm run test   # <-- Add this line to run tests during build
RUN npm run build

FROM nginx:alpine
COPY --from=build /app/dist /usr/share/nginx/html


#