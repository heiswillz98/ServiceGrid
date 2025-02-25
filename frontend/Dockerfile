# frontend/Dockerfile
FROM node:14
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
ENV PORT=8080
ENV AUTH_API_ADDRESS=http://auth-api:8081
ENV TODOS_API_ADDRESS=http://todos-api:8082
EXPOSE 8080
CMD ["npm", "run", "dev"]