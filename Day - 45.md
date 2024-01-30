Daily Notes : Day 45 
CSRF BYPASSES
1: Change the request Method
2: Remove CSRF parameter 
3: Remove the Referer Header
4: Double Cookie Submit ( the server does not keep a record of CSRF tokens. The CSRF token is just a copy of the session cookie )
5: Replace token with Same length value
6: Decoding CSRF tokens
7: only use the static parts of the token
8: Change Content type