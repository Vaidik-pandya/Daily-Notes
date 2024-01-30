Daily Notes : Day 76
what you can do on Password reset ?

1. Change the request method and content-type and observer how the application is responding.
2. Append null bytes after your email and observe the response.
3. Try XSS, SSTI etc in the email field.
4. Try Command injection
5. 2FA auto disabled after password reset.
6.User Enumeration.
7. Check whether any param value is reflecting in the email. Now try HTMLi.
8.XXE (if forgot-password request accepts xml).
9.Missing Rate Limit - Email triggering.