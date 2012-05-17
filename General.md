General Rules
=============

Protocol
--------
**Omit the protocol from embedded resources.**

Omit the protocol portion (http:, https:) from URLs pointing to images and other media files, style sheets, and scripts unless the respective files are not available over both protocols.

Omitting the protocol—which makes the URL relative—prevents mixed content issues and results in minor file size savings.

**Important: this does not apply to full URLs used for links and form actions. Please ensure http: or https: are applied appropriately to prevent security issues.**

	<!-- Not recommended -->
	<script src="http://www.google.com/js/gweb/analytics/autotrack.js"></script>
	<!-- Recommended -->
	<script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>
	/* Not recommended */
	.example {
		background: url(http://www.google.com/images/example);
	}
	/* Recommended */
	.example {
		background: url(//www.google.com/images/example);
	}


Formatting Rules
================

Indentation
-----------
*\*In Flux\** **Indent by 1 tab at a time.**

Don’t use spaces or mix tabs and spaces for indentation.

The tab width is assumed to 4 spaces.

	<ul>
		<li>Fantastic
		<li>Great
	</ul>
	.example {
		color: blue;
	}


Capitalization
--------------
**Use only lowercase.**

All code has to be lowercase: this applies to element names, attributes, attribute values (unless text/CDATA), selectors, properties, and property values (with the exception of strings).

	<!-- Not recommended -->
	<A HREF="/">Home</A>
	<!-- Recommended -->
	<img src="google.png" alt="Google">


Trailing whitespace
-------------------
**Remove trailing white spaces.**

Trailing white spaces are unnecessary and can complicate diffs.

	<!-- Not recommended -->
	<p>What?_
	<!-- Recommended -->
	<p>Yes please.
	General Meta Rules


Encoding
--------
**Use UTF-8 (no BOM).**

Make sure your editor uses UTF-8 as character encoding, without a byte order mark.

Specify the encoding in HTML templates and documents via `<meta charset="utf-8">`. Do not specify the encoding of style sheets as these assume UTF-8.

(More on encodings and when and how to specify them can be found in Character Sets & Encodings in XHTML, HTML and CSS.)


Comments
--------
**Explain code as needed, where possible.**

Use comments to explain code: what does it cover, what purpose does it serve, why is respective solution used or preferred?

(This item is optional as it is not deemed a realistic expectation to always demand fully documented code. Mileage may vary heavily for HTML and CSS code and depends on the project’s complexity.)


Action items
------------
**Mark todos and action items with TODO.**

Highlight todos by using the keyword TODO only, not other common formats like @@.

Append action items after a colon as in TODO: action item.

	{# TODO: revisit centering #}
	<center>Test</center>
	<!-- TODO: remove optional tags -->
	<ul>
		<li>Apples</li>
		<li>Oranges</li>
	</ul>


File Naming
-----------
*\*In Flux\** TODO
