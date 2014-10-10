# Events XML XSLT Etc #

## Eweb ##

- Event info 2014
	- One control - XSLGenerator.ascx
	- XSLGenerator part of netForum
	- Assemble HTML anywhere
	- mostly in eWEb
	- wiki.avectra.com
		- xslGenerator

`
{BeginXMLBuilderXML}
<xml>
DECLARE @evt_key nvarchar(38)
SET @evt_key = {evt_key}

- goes to a stored procedure (by William)
	- client_4as_xml_event_info @evt_key
	- includes schema.org
- data in netForum
- exported as XML
- XSL applied by netForum control
- resulting HTML "published" through the eWeb template


