Daily Notes : Day 72  
Subdomain gathering Methods!

1.  
https://asn.cymru.com/cgi-bin/whois.cgi  
https://bgp.he.net

2\. amass intel -asn &lt;ASN_ID&gt; -ip

3\. python3 http://san.py &lt;domain&gt;  
https://github.com/appsecco/the-art-of-subdomain-enumeration/blob/master/san_subdomain_enum.py

4\. curl --head -s -L http://domain.com | grep -iE "Content-Security-Policy|CSP"

5\. Third Party  
VirusTotal  
DNSDumpster  
Findomain

6\. amass enum --passive -d http://domain.com

7\. Transprancy  
https://crt.sh  
https://censys.io  
https://developers.facebook.com/tools/ct/