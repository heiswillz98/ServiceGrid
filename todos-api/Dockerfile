# todos-api/Dockerfile
FROM node:8
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
ENV JWT_SECRET=myfancysecret
ENV REDIS_HOST=redis-queue
ENV REDIS_PORT=6379
ENV REDIS_CHANNEL=log_channel
EXPOSE 8082
CMD ["npm", "start"]