<!-- markdownlint-disable -->
<img alt="Starlite logo" src="./static/starlite-banner.svg" width="100%" height="auto">
<!-- markdownlint-restore -->

<div align="center">

[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=coverage)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Technical Debt](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=sqale_index)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=sqale_rating)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=vulnerabilities)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)
[![Bugs](https://sonarcloud.io/api/project_badges/measure?project=starlite-api_starlite-pg-redis-docker&metric=bugs)](https://sonarcloud.io/summary/new_code?id=starlite-api_starlite-pg-redis-docker)

</div>

# starlite-pg-redis-docker

This is an example [Starlite](https://github.com/starlite-api/starlite) project using SQLAlchemy + Alembic + postgresql,
Redis and Docker.

## Starlite

Starlite is a light and flexible ASGI API framework.

[Starlite documentation 📚](https://starlite-api.github.io/starlite/)

### Setup

- `pre-commit install`
- `$ cp .env.example .env`
- `$ docker-compose build`
- `$ docker-compose run --rm app alembic upgrade head`

### Run

`$ docker-compose up --build`

### Migrations

#### Revision

`$ docker-compose run --rm app alembic revision --autogenerate -m "revision description"`

#### Migration

`$ docker-compose run --rm app alembic upgrade head`

### Test

`$ poetry run pytest`

### Linting

`$ pre-commit run --all-files`

### Add Dependencies

#### Production

`$ poetry add starlite`

#### Dev

`$ poetry add starlite --extras=testing --dev`
