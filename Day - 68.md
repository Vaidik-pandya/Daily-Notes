Daily Notes : Day 68
SSH attacks - part 2

Root login
By default most SSH server implementation will allow root login, it is advised to disable it because if the credentials of this accounts leaks, attackers will get administrative privileges directly and this will also allow attackers to conduct bruteforce attacks on this account.

SFTP command execution
Another common SSH misconfiguration is often seen in SFTP configuration. Most of the time when creating a SFTP server the administrator want users to have a SFTP access to share files but not to get a remote shell on the machine.

SFTP Tunneling
If you have access to a SFTP server you can also tunnel your traffic through this

Authentication methods
On high security environment it’s a common practice to enable only key-based or two factor authentication rather than the simple factor password based authentication. But often the stronger authentication methods are enabled without disabling the weaker ones. A frequent case is enabling publickey on openSSH configuration and setting it as the default method but not disabling password.