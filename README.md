# sqlcheatsheet

##How to install PostgreSQL
####FROM a terminal window, run `brew install postgres`

##How to create a database:
####Once PostgreSQL is installed (see above), run the following FROM a terminal window:
```
createdb dbname
```

##To connect to the db
####Once the db has been created, run the following FROM a terminal window:
```
psql dbname
```

##Useful psql commands

####To see available dbs:
```
\l
```

####To connect to a db:
```
\c dbname
```

####To list the tables of the currently connected db:
```
\dt
```

####To exit back to the terminal window:
```
\q
```

##SQL commands inside psql:

####To return all columns and rows from a particular table:
```
SELECT * FROM tablename;
```

####To return only certain columns (but all rows) from a particular table:
```
SELECT columnName1 (, columnName2, columnName3, etc) FROM tablename;
```

####To return only rows containing specific data:
```
SELECT * FROM tablename WHERE condition // columnName = value;
```
####You can have multiple conditions for a WHERE clause, just separate each one with the word AND

####To insert data into a table:
```
INSERT INTO tablename (columnName1, columnName2, etc.) VALUES (value1, value2, etc.);
```

####To update a record in a table:
```
UPDATE tablename SET columnName1 = value1 (, columnName2 = value2, etc.) WHERE condition;
```

####To remove a row FROM a table:
```
DELETE FROM tablename WHERE condition;
```

####To retrieve a specific part of a date field (ie, show the year):
```
SELECT date_part('unit', date(date_column)) FROM tablename;
```
#####'Unit' is a predefined abbreviation depending on what you are trying to display. See [Table 8-1. Data Types](https://www.postgresql.org/docs/current/static/datatype.html#DATATYPE-TABLE) for a list of possibilities.

# sqlcheatsheet
# sqlcheatsheet
