Daily Notes : Day 79 
File Upload Escalation: 

1. Set filename to ../../../tmp/lol.png and try to achieve a path traversal
2. Set filename to sleep(10)-- -.jpg and you may be able to achieve a SQL injection
3. Set filename to <svg onload=alert(document.domain)> to achieve a XSS
4. Set filename to ; sleep 10; to test some command injection (https://book.hacktricks.xyz/pentesting-web/command-injection)
5. ⁠JS file upload + XSS  (https://book.hacktricks.xyz/pentesting-web/xss-cross-site-scripting#xss-abusing-service-workers)
6. ⁠ you can indicate the web server to catch an image from a URL you could try to abuse a SSRF. If this image is going to be saved in some public site, you could also indicate a URL from https://iplogger.org/invisible/ and steal information of every visitor.

Reference: hacktricks