Daily Notes : Day 51 
DNS REBINDING -Part 1

DNS Rebidding + TLS Session ID/Session ticket

Requirements:
SSRF
Outbound TLS sessions
Stuff on local ports

Attack:
Ask the user/bot access a domain controlled by the attacker
The TTL of the DNS is 0 sec (so the victim will check the IP of the domain again soon)
A TLS connection is created between the victim and the domain of the attacker. The attacker introduces the payload inside the Session ID or Session Ticket.
The domain will start an infinite loop of redirects against himself. The goal of this is to make the user/bot access the domain until it perform again a DNS request of the domain.
In the DNS request a private IP address is given now (127.0.0.1 for example)
The user/bot will try to reestablish the TLS connection and in order to do so it will send the Session ID/Ticket ID (where the payload of the attacker was contained). So congratulations you managed to ask the user/bot attack himself.
Note that during this attack, if you want to attack localhost:11211 (memcache) you need to make the victim establish the initial connection with http://attacker.com:11211 (the port must always be the same).
To perform this attack you can use the tool: 