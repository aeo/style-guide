CSS Style Rules

CSS validity

link ▽ Use valid CSS where possible.
Unless dealing with CSS validator bugs or requiring proprietary syntax, use valid CSS code.

Use tools such as the W3C CSS validator to test.

Using valid CSS is a measurable baseline quality attribute that allows to spot CSS code that may not have any effect and can be removed, and that ensures proper CSS usage.

ID and class naming

link ▽ Use meaningful or generic ID and class names.
Instead of presentational or cryptic names, always use ID and class names that reflect the purpose of the element in question, or that are otherwise generic.

Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.

Generic names are simply a fallback for elements that have no particular or no meaning different from their siblings. They are typically needed as “helpers.”

Using functional or generic names reduces the probability of unnecessary document or template changes.

/* Not recommended: meaningless */
#yee-1901 {}

/* Not recommended: presentational */
.button-green {}
.clear {}
/* Recommended: specific */
#gallery {}
#login {}
.video {}

/* Recommended: generic */
.aux {}
.alt {}
ID and class name style

link ▽ Use ID and class names that are as short as possible but as long as necessary.
Try to convey what an ID or class is about while being as brief as possible.

Using ID and class names this way contributes to acceptable levels of understandability and code efficiency.

/* Not recommended */
#navigation {}
.atr {}
/* Recommended */
#nav {}
.author {}
Type selectors

link ▽ Avoid qualifying ID and class names with type selectors.
Unless necessary (for example with helper classes), do not use element names in conjunction with IDs or classes.

Avoiding unnecessary ancestor selectors is useful for performance reasons.

/* Not recommended */
ul#example {}
div.error {}
/* Recommended */
#example {}
.error {}
Shorthand properties

link ▽ Use shorthand properties where possible.
CSS offers a variety of shorthand properties (like font) that should be used whenever possible, even in cases where only one value is explicitly set.

Using shorthand properties is useful for code efficiency and understandability.

/* Not recommended */
border-top-style: none;
font-family: palatino, georgia, serif;
font-size: 100%;
line-height: 1.6;
padding-bottom: 2em;
padding-left: 1em;
padding-right: 1em;
padding-top: 0;
/* Recommended */
border-top: 0;
font: 100%/1.6 palatino, georgia, serif;
padding: 0 1em 2em;
0 and units

link ▽ Omit unit specification after “0” values.
Do not use units after 0 values unless they are required.

margin: 0;
padding: 0;
Leading 0s

link ▽ Omit leading “0”s in values.
Do not use put 0s in front of values or lengths between -1 and 1.

font-size: .8em;
Quotation marks in URI values

link ▽ Omit quotation marks in URI values.
Do not use quotation marks ("", '') with url().

@import url(//www.google.com/css/go.css);
Hexadecimal notation

link ▽ Use 3 character hexadecimal notation where possible.
For color values that permit it, 3 character hexadecimal notation is shorter and more succinct.

/* Not recommended */
color: #eebbcc;
/* Recommended */
color: #ebc;
Prefixes

link ▽ Prefix selectors with an application-specific prefix (optional).
In large projects as well as for code that gets embedded in other projects or on external sites use prefixes (as namespaces) for ID and class names. Use short, unique identifiers followed by a dash.

Using namespaces helps preventing naming conflicts and can make maintenance easier, for example in search and replace operations.

.adw-help {} /* AdWords */
#maia-note {} /* Maia */
ID and class name delimiters

link ▽ Separate words in ID and class names by a hyphen.
Do not concatenate words and abbreviations in selectors by any characters (including none at all) other than hyphens, in order to improve understanding and scannability.

/* Not recommended: does not separate the words “demo” and “image” */
.demoimage {}

/* Not recommended: uses underscore instead of hyphen */
.error_status {}
/* Recommended */
#video-id {}
.ads-sample {}
Hacks

link ▽ Avoid user agent detection as well as CSS “hacks”—try a different approach first.
It is tempting to address styling differences over user agent detection or special CSS filters, workarounds, and hacks. Both approaches should be considered last resort in order to achieve and maintain an efficient and manageable code base. Put another way, giving detection and hacks a free pass will hurt projects in the long run as projects tend to take the way of least resistance. That is, allowing and making it easy to use detection and hacks means using detection and hacks more frequently—and more frequently is too frequently.

CSS Formatting Rules

Declaration order

link ▽ Alphabetize declarations.
Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain.

Ignore vendor-specific prefixes for sorting purposes. However, multiple vendor-specific prefixes for a certain CSS property should be kept sorted (e.g. -moz prefix comes before -webkit).

background: fuchsia;
border: 1px solid;
-moz-border-radius: 4px;
-webkit-border-radius: 4px;
border-radius: 4px;
color: black;
text-align: center;
text-indent: 2em;
Block content indentation

link ▽ Indent all block content.
Indent all block content, that is rules within rules as well as declarations, so to reflect hierarchy and improve understanding.

@media screen, projection {

  html {
    background: #fff;
    color: #444;
  }

}
Declaration stops

link ▽ Use a semicolon after every declaration.
End every declaration with a semicolon for consistency and extensibility reasons.

/* Not recommended */
.test {
  display: block;
  height: 100px
}
/* Recommended */
.test {
  display: block;
  height: 100px;
}
Property name stops

link ▽ Use a space after a property name’s colon.
Always use a single space between property and value (but no space between property and colon) for consistency reasons.

/* Not recommended */
h3 {
  font-weight:bold;
}
/* Recommended */
h3 {
  font-weight: bold;
}
Selector and declaration separation

link ▽ Separate selectors and declarations by new lines.
Always start a new line for each selector and declaration.

/* Not recommended */
a:focus, a:active {
  position: relative; top: 1px;
}
/* Recommended */
h1,
h2,
h3 {
  font-weight: normal;
  line-height: 1.2;
}
Rule separation

link ▽ Separate rules by new lines.
Always put a line between rules.

html {
  background: #fff;
}

body {
  margin: auto;
  width: 50%;
}
CSS Meta Rules

Section comments

link ▽ Group sections by a section comment (optional).
If possible, group style sheets sections together by using comments. Separate sections with new lines.

/* Header */

#adw-header {}

/* Footer */

#adw-footer {}

/* Gallery */

.adw-gallery {}
