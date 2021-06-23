# RabbitMQ

A central rabbitmq service. RabbitMQ is an event broker for inter-service communication.

# Running

Copy the env file:

`cp .env.example .env`

Edit the .env file

`nano .env`

Fill out the related fields:

```
RABBITMQ_DEFAULT_USER=
RABBITMQ_DEFAULT_PASS=
```

Run the container:

`docker-compose up`


