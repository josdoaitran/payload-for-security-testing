# How to Test for Path Traversal Vulnerabilities

## OWASP
See the OWASP Testing Guide article on how to Test for Path Traversal Vulnerabilities.

**Description**

* Request variations
Encoding and double encoding:

```
%2e%2e%2f represents ../
%2e%2e/ represents ../
..%2f represents ../ 
%2e%2e%5c represents ..\
%2e%2e\ represents ..\ 
..%5c represents ..\ 
%252e%252e%255c represents ..\ 
..%255c represents ..\ and so on. 
```
* Percent encoding (aka URL encoding)

Note that web containers perform one level of decoding on percent encoded values from forms and URLs.
```
..%c0%af represents ../ 
..%c1%9c represents ..\ 
```

* OS specific

_UNIX_
```
Root directory:  “ / “ 
Directory separator: “ / “
```
_WINDOWS_
```
Root directory: “  <partition letter> : \ “
Directory separator: “ / “ or “ \ ” 
Note that windows allows filenames to be followed by extra . \ / characters.
```
In many operating systems, null bytes %00 can be injected to terminate the filename. For example, sending a parameter like:
```
?file=secret.doc%00.pdf
```

will result in the Java application seeing a string that ends with ".pdf" and the operating system will see a file that ends in ".doc". Attackers may use this trick to bypass validation routines.

## Local/Remote File Inclusion

The File Inclusion vulnerability allows an attacker to include a file, usually exploiting a "dynamic file inclusion" mechanisms implemented in the target application.

Interesting files to check out :

```

```

# Reference

* https://www.owasp.org/index.php/Path_Traversal
* 