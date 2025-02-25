# auth-api/Dockerfile
FROM golang:1.21
WORKDIR /app
COPY . .
RUN go mod download
RUN go build -o auth-api .
ENV AUTH_API_PORT=8081
ENV USERS_API_ADDRESS=http://users-api:8083
ENV JWT_SECRET=myfancysecret
EXPOSE 8081
CMD ["./auth-api"]