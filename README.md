# Hydra
This repository contains Hydra codebase.

### Development
We use docker and docker-compose to run our application in an isolated environment.
You can just execute standart docker-compose commands to interact with containers.
Check the [docker-compose.yml](docker-compose.yml) to see the configuration.

### Docker Compose
- Start application: `docker-compose up`
- Stop application: `docker-compose stop`
- Rebuild and start application: `docker-compose up --build`
- Drop everything for a fresh start: `docker-compose down --rmi all -v --remove-orphans`
- Enter to a running container: `docker-compose exec {container} /bin/sh`
- Enter to the postgres psql: `docker-compose exec postgres psql`
- Create a database dump: `docker-compose exec postgres pg_dump > dump.sql`
- Restore a database dump: `cat dump.sql | docker exec -i $(docker-compose ps -q postgres) psql`
