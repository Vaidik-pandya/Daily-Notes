Daily Notes : Day 67 
SMTP pentesting 

SMTP (Simple Mail Transfer Protocol) is a TCP/IP protocol used in sending and receiving e-mail. However, since it is limited in its ability to queue messages at the receiving end, it is usually used with one of two other protocols, POP3 or IMAP, that let the user save messages in a server mailbox and download them periodically from the server.

Metasploit : 

Metasploit:%20auxiliary/scanner/smtp/smtp_enum%0Asmtp-user-enum:%20smtp-user-enum%20-M%20%3CMODE%3E%20-u%20%3CUSER%3E%20-t%20%3CIP%3E%0ANmap:%20nmap%20--script%20smtp-enum-users%20%3CIP%3E

Check all attack: 

https://t.co/MqGTbZJ3T7