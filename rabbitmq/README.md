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


## Adding a service

To configure a service to be connected to the RabbitMQ event broker, add it to the `network-events` network. You can then use `rabbitmq` as the IP address of the broker.


```yaml
services:
    your_service:
        networks:
            - network-events
networks:
  network-events:
    external:
      name: network-events
```