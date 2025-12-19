/**
# Documentation

## Prerequisites
- **PostgreSQL**: Ensure you have a running PostgreSQL instance.
- **Go**: Install Go from [https://golang.org/dl/](https://golang.org/dl/).

## Installing the `gator` CLI
To install the `gator` CLI, run:
```sh
go install github.com/codrinursachi/gator
```
This will place the `gator` binary in your `$GOPATH/bin` directory.

## Configuration
1. Create a global configuration file at `~/.gatorconfig.json`.
2. Specify your database connection and other required settings.
    Example (`~/.gatorconfig.json`):
    ```json
    {
      "db_url": "postgres://postgres:postgres@localhost:5432/gator?sslmode=disable",
      "current_user_name": "kahya"
    }
    ```

## Running the Program
1. Ensure your PostgreSQL server is running and accessible.
2. Run the program using:
    ```sh
    go run main.go <command> [args...]
    ```

## Available Commands

- `login`: Log in as a user.
- `register`: Register a new user.
- `reset`: Reset user password or state.
- `users`: List all users.
- `agg`: Run aggregation queries.
- `addfeed`: Add a new feed (requires login).
- `feeds`: List available feeds.
- `follow`: Follow a feed (requires login).
- `following`: List feeds you are following (requires login).
- `unfollow`: Unfollow a feed (requires login).