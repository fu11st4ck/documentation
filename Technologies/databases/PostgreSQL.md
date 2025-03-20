# PostgreSQL
We use `person` table with `first_name`, `last_name`, `gender`, `email`, `date_of_birth` and `country_of_birth` columns to demonstrate the tutorial.

## Sample queries
### Create `Person` table:
Below is the sample query to create person tatble with `id`, `first_name`, `last_name`, `email`, `gender`, `date_of_birth` and `country_of_birth`. 
```sql
CREATE TABLE person (
	id BIGSERIAL NOT NULL PRIMARY KEY,
	first_name VARCHAR(50) NOT NULL,
	last_name VARCHAR(50) NOT NULL,
	email VARCHAR(150),
	gender VARCHAR(25) NOT NULL,
	date_of_birth DATE NOT NULL,
	country_of_birth VARCHAR(50)
);
```

### Insert data into `person` table:
Below is the sample query to insert data into all columns of the `person` table.
```sql
INSERT INTO person (first_name, last_name, email, gender, date_of_birth, country_of_birth) VALUES ('Zita', 'Tarbatt', 'ztarbatt0@1688.com', 'Female', '1991-10-20', 'Kazakhstan');
```

## Limit, Offset & Fetch
### Limit:
To select specific amount of records from the table, in this case we are going to select first 10 records from the `person` table.
```sql
SELECT * FROM person LIMIT 10; 
```

### Offset:
Offset will be used to skip specific amount of records, in this case we are going to skip first 10 record and select 10 records after that from the `person` table. It is used to create pagination functionality in real case scenario.
```sql
SELECT * FROM person OFFSET 10 LIMIT 10;
```