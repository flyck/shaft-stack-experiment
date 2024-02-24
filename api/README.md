# Api

To install dependencies:

```bash
bun install
```

This project was created using `bun init` in bun v1.0.21. [Bun](https://bun.sh) is a fast all-in-one JavaScript runtime.

## Dev Notes

- tuqls sequelize had issues on my Mac M1
  - just install sqlite3 seperately and it works


## Sqlite Setup

Create a new database:
```sh
sqlite3 db.sqlite
```


Create the tables:
```sql
create table parties(
  id integer not null primary key autoincrement,
  title text not null,
  description text,
  location text,
  date text
);
create table participants(
  id integer not null primary key autoincrement,
  party_id varchar(6) not null,
  name text not null,
  email text,
  invitation_sent boolean not null,
  foreign key (party_id)
       references parties (id) on delete cascade
);
```

Dummy data:
```sql
INSERT INTO parties (title, description, location, date) VALUES
('Birthday Bash', 'Celebrating a special day!', '123 Main Street', '2024-02-18'),
('Office Christmas Party', 'Year-end festivities', '456 Business Ave', '2024-12-20'),
('Summer BBQ', 'Grilling and chilling', '789 Sunny Lane', '2024-07-15');

INSERT INTO participants (party_id, name, email, invitation_sent) VALUES
(1, 'John Doe', 'john@example.com', 1),
(1, 'Jane Smith', 'jane@example.com', 0),
(2, 'Bob Johnson', 'bob@example.com', 1),
(3, 'Alice Anderson', 'alice@example.com', 0),
(3, 'Charlie Brown', 'charlie@example.com', 1);
```

Exit:
```sh
.exit
```
