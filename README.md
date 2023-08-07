# README

## Setup

This application was tested on macOS Venture 13.5.

Ruby 3.2.2 was provided via `rbenv`.

This application assumes you have installed PostgreSQL 14 via Homebrew:

```
brew install postgresql@14
brew link postgresql@14
```

This application requires a PostgreSQL database server. You can use a Docker container or Homebrew to provide one.

Docker:

```
docker run -it -p 5432:5432 -e POSTGRES_PASSWORD=password postgres:14.5
```

Homebrew:

```
/opt/homebrew/opt/postgresql@14/bin/postgres -D /opt/homebrew/var/postgresql@14
```

This application assumes your Postgres server is running on `localhost:5432` with a username of `postgres` and a password of `password`. 
If that is not the case, set the `DATABASE_URL` environment variable with an appropriate connection string.

## Running Tests

Run `spring stop` to ensure Spring has stopped. Then run `rake test` to induce failure.
