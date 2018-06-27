# How to Test for Path Traversal Vulnerabilities
See the OWASP Testing Guide article on how to Test for Path Traversal Vulnerabilities.
Description
Request variations
Encoding and double encoding:

,,,
%2e%2e%2f represents ../
%2e%2e/ represents ../
..%2f represents ../ 
%2e%2e%5c represents ..\
%2e%2e\ represents ..\ 
..%5c represents ..\ 
%252e%252e%255c represents ..\ 
..%255c represents ..\ and so on. 
,,,

# Reference

* https://www.owasp.org/index.php/Path_Traversal