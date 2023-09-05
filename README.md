# natsume

This is sandbox for Database.

## How to use
### Install SQlite3

```console
sudo apt-get install -y sqlite3
```

### Create tables

```console
sqlite3 ./natsume.sqlite
```

```console
CREATE TABLE books (
  id INTEGER PRIMARY KEY,
  title TEXT,
  author TEXT
);
```

### Insert from CSV file

```console
sqlite3 ./natsume.sqlite
```

```console
.mode csv
.import books.csv books
```
