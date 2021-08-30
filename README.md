# Docker-compose project for Authz POC (Keycloak - ORY Keto - OPA - Secured API)

A compose file that will build some projects and deploy them together so the POC can be executed

## How to execute

```shell script
docker-compose up
```

This will create these services:

- Postgres for ORY Keto
- An ephemeral ORY Keto database migration script that will create the tables for Keto to work with your namespaces.
- ORY Keto
- Keycloak with a custom EventsListener SPI that will send events to ORY Keto.
- OPA with a custom built-in function that will call ORY Keto for a check.
- A Quarkus REST API that we want to secure. This will serve a bundle to OPA with policies and relations data for internal querying.

## What does the POC do?

TBD