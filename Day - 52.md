Daily Notes : Day 52 
One liners - part 1

1: Subdomain from security trails 
curl -s "https://securitytrails.com/list/apex_domain/HOST" | grep -Po "((http|https):\/\/)?(([\w.-]*)\.([\w]*)\.([A-z]))\w+" | grep ".HOST" | sort -u

2: Subdomains With http://sonar.omnisint.io
curl --silent https://sonar.omnisint.io/subdomains/HOST | grep -oE "[a-zA-Z0-9._-]+\.HOST" | sort -u

3: Subdomains from Archive
curl -s "http://web.archive.org/cdx/search/cdx?url=*.HOST/*&output=text&fl=original&collapse=urlkey" | sed -e 's_https*://__' -e "s/\/.*//" | sort -u

4: Find Allocated IP Ranges for ASN from IP Address
whois -h http://whois.radb.net -i origin -T route $(whois -h http://whois.radb.net IP | grep origin: | awk '{print $NF}' | head -1) | grep -w "route:" | awk '{print $NF}' | sort -n

Ref: https://github.com/dwisiswant0/awesome-oneliner-bugbounty
