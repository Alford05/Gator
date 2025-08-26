# Gator

 A command-line tool for aggregating RSS feeds and viewing posts 

 ## Installation

 Ensure you have the latest Go toolchain (https://golang.org/dl/) installed 
 as well as a local Postgres database. You can then install `gator` with:

```bash
go install github.com/your-username/gator@latest
```
# ensure $GOPATH/bin (or $HOME/go/bin) is on your PATH

## Config

Create $HOME/.gatorconfig.json:

```
{
  "db_url": "postgres://USER:PASSWORD@localhost:5432/DBNAME?sslmode=disable"
}
```

Replace the value with your database connection string

## Usage

Create a new User:
```bash
gator register <name>
```

Add a feed:
```bash
gator addfeed <url>
```

Start the aggregator:
```bash
gator agg 30s
```

View the posts:
```bash
gator browse [limit]
```

Other commands that can be used include:
- `gator login <name>` - Log in as a user that already exists
- `gator users` - List all users
- `gator feeds` - List all feeds
- `gator follow <url>` - Follow a feed that already exists in the database
- `gator unfollow <url>` - Unfollow a feed that already exists in the database

Dev vs Prod:
Development: go run .
Production: gator

# Publish 
https://github.com/Alford05/Gator
