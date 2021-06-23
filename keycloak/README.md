# Keycloak

This deploys a keycloak server onto the network. Copy `.env.example` to `.env`, and fill out the related details.

By default, this uses the central `mysql` service as the backend. See the `mysql` service for information about the database.

# Running

Copy the env file:

`cp .env.example .env`

Edit the .env file

`nano .env`

Fill out the related fields:

```
DB_VENDOR=
DB_ADDR=
DB_DATABASE=
DB_USER=
DB_PASSWORD=
KEYCLOAK_USER=
KEYCLOAK_PASSWORD=
JDBC_PARAMS=
VIRTUAL_PORT=
VIRTUAL_HOST=
```

Build the container:

`docker-compose build`

Run the container:

`docker-compose up`


