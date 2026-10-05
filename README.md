# service-docker-multiplayer-fabric

Container images and a compose file for a zone-server stack: a database, object storage, the Uro API server and scalable zone processes.

## What it is for

The compose file starts a database, object storage, the Uro API server and one headless engine process per zone container. Docker assigns each zone replica its host UDP port, and Uro discovers that port through the Docker socket and manages the zone's lifecycle. The Dockerfiles build the zone image, the Uro image and an export baker from source checkouts the build supplies as contexts.

## Run it

Load the database image first, as the comment on the compose file's database service says. Then set the environment variables the compose file's header lists and run:

```sh
docker compose up
```

## Licence

The licence is not stated.
