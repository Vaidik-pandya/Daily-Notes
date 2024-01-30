Daily Notes : Day 69 
Nmap Oneliners 

# Pull Resolved Hosts From .gnmap Files
grep "Host: " *.gnmap|sed 's/\t/ /g'|tr -s '[:space:]'|cut -d" " -f3|awk '!/\(\)/'|sort -u|sed 's/(//g;s/)//g'

# Pull Alive Host IPs Based on Open Port From .gnmap Files
grep "Host:.*Ports:.*/open/" *.gnmap|cut -d" " -f2

# Pull Alive Host IPs Based on Status Form .gnmap Files (Varying Results Based On Scan Flags [i.e.: -Pn])
grep "Host:.*Status: Up" *.gnmap|cut -d" " -f2

# Common Discovery Scan String (Known RTT)
nmap -Pn -R -sS -p 21-23,25,53,111,137,139,445,80,443,3389,5900,8080,8443 --min-rtt-timeout <Lowest RTT Time + 25ms> \
     --max-rtt-timeout <Highest RTT Time + 100ms> --max-retries 1 --max-scan-delay 0 -oA <Output Filename> -vvv \
     --open -iL <Host List>

# Common Discovery Scan String (Unknown RTT)
nmap -Pn -R -sS -p 21-23,25,53,111,137,139,445,80,443,3389,5900,8080,8443 --max-retries 1 \
     --max-scan-delay 0 -oA <Output Filename> -vvv --open -iL <Host List>

https://gist.github.com/sente/eb52bfceafe2abec4011