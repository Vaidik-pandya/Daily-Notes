Daily Notes : Day 85 
CSRF - Bypasses 

1. Remove the entire token parameter with value/Remove just the value.
2. Use any other random but same length token.
3. Use any other random (length-1) or (length+1) token.
4. Use attacker's token in victim's session.
5. Change the method from POST to GET and remove the token.
6. If request is made through PUT or DELETE then try POST 
7. If token is sent through custom header; try to remove the header.
8. Change the Content-Type to application/json, application/x-url-encoded or form-multipart, text/xml, application/xml.
9. If double submit token is there (in cookies and some header) then try CRLF injection.
10. Bypassing referrer check:  
i. If the referrer header is checked but only when it exists in the request then add this piece of code in your csrf poc: ```<meta name="referrer" content="never">```  
ii. Regex Referral bypass:  
11. CSRF token stealing via xss/htmli/cors.
12. JSON Based:  
i. Change the Content-Type to text/plain, application/x-www-form-urlencoded, multipart/form-data and check if it accepts.  
ii. Use flash + 307 redirect.
13. Guessable CSRF token.
14. Clickjacking to strong CSRF token bypass.
15. Type Juggling.
16. Array: newemail=victim@gmail.com&csrftoken[]=lol
17. Set the csrf token to "null" or add null bytes.
18. Check whether csrf token is sent over http or sent to 3rd party. See [here](https://hackerone.com/reports/15412)
19. Generate multiple csrf tokens, observe the static part. Keep it as it is and play with the dynamic part.