FROM python:3.10
WORKDIR /app
RUN apt-get update && apt-get install -y python3-distutils
COPY requirements.txt .
RUN pip install --upgrade pip && pip install -r requirements.txt
COPY . .
ENV REDIS_HOST=redis-queue
ENV REDIS_PORT=6379
ENV REDIS_CHANNEL=log_channel
CMD ["python3", "main.py"]