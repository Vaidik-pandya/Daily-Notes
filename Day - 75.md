Daily Notes : Day 75
Denial of Service - Part 2

1. Abusing Referrer cookie: Application uses WAF which blocks user on using some XSS/SQLi payloads + stores referrer URL value in cookies.

2. Try null bytes (%00, %0d%0a, %0d, %0a, %09, %0C, %20) in different input fields.

3. If the application is using JSON, try using null as a value of some input field.

4. Dos via Web Cache Poisoning: In case, you are able to redirect users by exploiting a web cache poisoning vulnerability, then try redirecting them to an invalid port (for example, http://example.com:1729)

5. pache HTTP Server Byte Range DoS: If the application is using Apache 1.3.x, 2.0.x<2.0.64, 2.2.X<2.2.19 then add this header to any request.

6. Missing rate limit on register/contact form → Memory corruption.

7. CPDoS (Cache Poisoned Denial of Service)