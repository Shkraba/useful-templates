version: '3.3'

services:
  redis:
    image: redis:latest
    restart: always
    ports:
      - "6379:6379"
    volumes:
      - /path/to/local/dаta:/root/redis
      - /path/to/local/redis.conf:/usr/local/etc/redis/redis.conf
    environment:
      - REDIS_PASSWORD=my-password
      - REDIS_PORT=6379
      - REDIS_DATABASES=1