# service-docker-multiplayer-fabric

Container images and a compose file for a zone-server stack: a database, object storage, the Uro API server and scalable zone processes.

## What it is for

The compose file starts a database, object storage, the Uro API server and one headless engine process per zone container, and Uro assigns each zone its UDP port and manages its lifecycle. The Dockerfiles build the zone image, the Uro image and an export baker from source checkouts the build supplies as contexts.

## Run it

Set the environment variables the compose file's header lists, then:

```sh
docker compose up
```

## Licence

The licence is not stated.
