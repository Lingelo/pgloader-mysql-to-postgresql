# Migrate from mysql to postreSQL with pgloader and docker

This repository allows you to switch from a MySQL database to a postgreSQL database very easily.

## Setup

* Clone repository.
* Put the dump file in the `migrations` folder. You can use the `migration.sql` file. Files in the `migrations` folder are launched on container initialization!
* Install everything via `docker-compose up -d`.

## Execute

Once the containers are launched, run:

`docker-compose exec postgres pgloader mysql://user:password@mysql:3306/database postgresql://postgres:root@localhost:5432/postgres`

Please note : `mysql://user:password@mysql:3306/database` can be overridden by your database access.

Et voilà, your database is migrated.
