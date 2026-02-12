# MySqlAudit

These are queries to help assist with retrieving users inside of a MySQL instance and the permissions that those users are assigned. These queries are designed to only read data and will not modify or create data inside of the database.

## MySQL Version

This query is designed to select the device hostname and database version.

```SQL
SELECT @@hostname, @@version_comment, VERSION();
```

## MySQL Global User Privileges

This query is designed to select information about global privileges granted to users.

```SQL
SELECT * FROM information_schema.user_privileges;
```

## MySQL Schema Privileges

This query is designed to select information about the schema (database) privileges.

```SQL
SELECT * FROM information_schema.schema_privileges;
```

## MySQL Table Privileges

This query is designed to select information about table-specific privileges for roles and users that are available or granted by the currently enabled roles.

```SQL
SELECT * FROM information_schema.table_privileges;
```

## MySQL Column Privileges

This query is designed to select information about column-specific privileges for roles and users that are available or granted by the currently enabled roles.

```SQL
SELECT * FROM information_schema.column_privileges;
```

## MySQL Role Assignments

This query is designed to select all role assignments that have been granted by currently enabled roles.

```SQL
SELECT * FROM mysql.role_edges;
```

## MySQL Table Role Grants

This query is designed to select information about the table privileges for roles that are available or granted by the currently enabled roles.

```SQL
SELECT * FROM information_schema.role_table_grants;
```

## MySQL Password Policy

This query is designed to select all system variables from the validate_password component.

```SQL
SHOW VARIABLES LIKE '%password%';
```
