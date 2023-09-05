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
sqlite> CREATE TABLE books (
  id INTEGER PRIMARY KEY,
  title TEXT,
  author TEXT
);

CREATE TABLE charpters (
  id INTEGER PRIMARY KEY,
  sort_number INTEGER,
  name TEXT,
  book_id INTEGER,
  FOREIGN KEY (book_id) REFERENCES books(id)
);
```

### Insert from CSV file

```console
sqlite> .import books.csv books --csv --skip 1
sqlite> .import chapters.csv charpters --csv --skip 1
```
