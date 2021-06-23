# MySQL

Central mysql database server for the home network.

## Running

Copy the env file:

`cp .env.example .env`

Edit the .env file

`nano .env`

Fill out the related fields:

```
MYSQL_USER=
MYSQL_ROOT_PASSWORD=
MYSQL_PASS=
```

Run the container:

`docker-compose up`

## Adding a service

To configure a service to be connected to the MySQL database, add it to the `network-database` network. You can then use `mysql` as the IP address of the database.


```yaml
services:
    your_service:
        networks:
            - network-database
networks:
  network-nginx-lan:
    external:
      name: network-database
```