# Docker-compose example

Here is an example on how to reproduce the Nhost stack from a docker-compose file.

## This is a fork filtered to get only the docker-compose portion

Awesome project [nhost](https://nhost.io/), check them out!

Note: Added Caddyfile incase we want to go with Caddy instead of Traefik

## Configuration

```sh
git clone https://github.com/ammarfaris/nhost-selfhost
cd nhost-selfhost
vim .env
vim docker-compose.yml
cd cert && vim ca-cert.crt
cd ..
docker compose up -d
```

OR

```sh
git clone https://github.com/ammarfaris/nhost-selfhost
cd nhost-selfhost
cp .env.example .env
vim docker-compose.yml
cd cert && vim ca-cert.crt
cd ..
docker compose up -d
```

The following endpoints are now exposed:

- `http://localhost:1337`: Hasura Console
- `http://localhost:1337/v1/graphql`: Hasura GraphQL endpoint
- `http://localhost:1337/v1/auth`: Hasura Auth
- `http://localhost:1337/v1/storage`: Hasura Storage
- `http://localhost:1337/v1/functions`: Functions

- `http://localhost:9090`: Traefik dashboad
- `http://localhost:8025`: Mailhog SMTP testing dashboard
