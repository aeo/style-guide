CSS Style Rules
===============

CSS Validity
------------
**Use valid CSS where possible.**

Unless dealing with CSS validator bugs or requiring proprietary syntax, use valid CSS code.

Use tools such as the W3C CSS validator to test.

Using valid CSS is a measurable baseline quality attribute that allows to spot CSS code that may not have any effect and can be removed, and that ensures proper CSS usage.


Using IDs
---------
**Do not use IDs for styling.**

IDs should never be used for styling purposes, use them as javascript hooks or for anchor tags. Class names can be identical to IDs if desired (eg. `<div id="warning_flag" class="warning_flag">`).

Reasons for this are to bring elements on the same plane in terms of CSS specificity, potential improved DOM selector performance (if less IDs exist) and appease CSS linter.

    /* Not recommended */
    #warning_flag {
      float: left;
      color: red;
    }

    /* Recommended */
    .warning_flag {
      float: left;
      color: red;
    }

    /* Also okay :) */
    <div id="warning_flag" class="warning_flag"></div>


Class Naming
------------
**Use meaningful or generic class names.**

Instead of presentational or cryptic names, always use class names that reflect the purpose of the element in question, or that are otherwise generic.

Names that are specific and reflect the purpose of the element should be preferred as these are most understandable and the least likely to change.

Generic names are simply a fallback for elements that have no particular or no meaning different from their siblings. They are typically needed as “helpers.”

Using functional or generic names reduces the probability of unnecessary document or template changes.

    /* Not recommended: meaningless */
    .yee_1901 {}

    /* Not recommended: presentational */
    .button_green {}
    .clear {}

    /* Recommended: specific */
    .gallery {}
    .login {}
    .video {}

    /* Recommended: generic */
    .aux {}
    .alt {}


Class Name Delimiters
---------------------
*\*In Flux** **Separate words in class names by a underscore.**

Do not concatenate words and abbreviations in selectors by any characters (including none at all) other than hyphens, in order to improve understanding and scannability.

    /* Not recommended: does not separate the words “demo” and “image” */
    .demoimage {}

    /* Not recommended: uses hyphen or camel-case instead of underscore */
    .error-status {}
    .testResult {}

    /* Recommended */
    .video_id {}
    .ads_sample {}


Prefixes
--------
**Prefix selectors with a context-specific prefix.**

Use prefixes as namespaces for class names. Use short, unique identifiers followed by an underscore.

Using namespaces helps preventing naming conflicts and can make maintenance easier, for example in search and replace operations.

Any classes used for Javascript should be prefixed with `js_`. These classes should be used **only** for Javascript (ie. no styles should be written against these classes).

Exceptions to this are classes meant to be _standard_ across the site (eg. `.strong_bttn`, `.input_field`).

    .adw_help {} /* AdWords */
    .maia_note {} /* Maia */

    .js_quickview {} /* Used only for Javascript event handling */


Class Name Style
----------------
**Use class names that are as short as possible but as long as necessary.**

Try to convey what an class is about while being as brief as possible.

Using class names this way contributes to acceptable levels of understandability and code efficiency.

    /* Not recommended */
    .navigation {}
    .atr {}

    /* Recommended */
    .nav {}
    .author {}


Type Selectors
--------------
**Avoid qualifying class names with type selectors.**

Unless necessary (for example with helper classes), do not use element names in conjunction with classes.

Avoiding unnecessary ancestor selectors is useful for performance reasons.

    /* Not recommended */
    ul.example {}
    div.error {}

    /* Recommended */
    .example {}
    .error {}


Shorthand Properties
--------------------
**Use shorthand properties where possible.**

CSS offers a variety of shorthand properties (like font) that should be used whenever possible, even in cases where only one value is explicitly set. The exception to this rule is that shorthand should not produce inheritance bugs (eg. using `background: url(...) no-repeat;` may clobber a necessary background-color).

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


0 and Units
-----------
**Omit unit specification after “0” values.**

Do not use units after 0 values unless they are required.

    margin: 0;
    padding: 0;


Leading 0s
----------
**Omit leading “0”s in values.**

Do not use put 0s in front of values or lengths between -1 and 1.

    font-size: .8em;


Quotation Marks in URI Values
-----------------------------
**Omit quotation marks in URI values.**

Do not use quotation marks ("", '') with url().

    background: url(//www.ae.com/Images/hello.png);


Hexadecimal Notation
--------------------
**Use hexadecimal notation and 3 character hexadecimal notation where possible.**

Do not use RGB, HSL, or color names. Use of RGBA is acceptable when opacity is used. Always write hexadecimal values in lowercase. For color values that permit it, 3 character hexadecimal notation is shorter and more succinct.

    /* Not recommended */
    color: rgb(65, 131, 196);
    color: green;
    color: #EEBBCC;

    /* Recommended */
    color: #4183C4;
    color: #0f0;
    color: #ebc;


Hacks
-----
**Avoid user agent detection as well as CSS “hacks”—try a different approach first.**

It is tempting to address styling differences over user agent detection or special CSS filters, workarounds, and hacks. Both approaches should be considered last resort in order to achieve and maintain an efficient and manageable code base. Put another way, giving detection and hacks a free pass will hurt projects in the long run as projects tend to take the way of least resistance. That is, allowing and making it easy to use detection and hacks means using detection and hacks more frequently—and more frequently is too frequently.


CSS Formatting Rules
====================

Declaration Order
-----------------
*\*In Flux** **Alphabetize declarations.**

Put declarations in alphabetical order in order to achieve consistent code in a way that is easy to remember and maintain.

Ignore vendor-specific prefixes for sorting purposes. However, multiple vendor-specific prefixes for a certain CSS property should be kept sorted (e.g. -moz prefix comes before -webkit).

    background: none;
    border: 1px solid;
    -moz-border-radius: 4px;
    -webkit-border-radius: 4px;
    border-radius: 4px;
    color: black;
    text-align: center;
    text-indent: 2em;


Block Content Indentation
-------------------------
**Indent all block content.**

Indent all block content, that is rules within rules as well as declarations, so to reflect hierarchy and improve understanding.

    @media screen, projection {

      html {
        background: #fff;
        color: #444;
      }

    }


Declaration Stops
-----------------
**Use a semicolon and a newline after every declaration.**

End every declaration with a semicolon and a newline for consistency and extensibility reasons.

    /* Not recommended */
    .test {
      display: block;
      height: 100px
    }

    .another_test { position: relative; z-index: 4; }

    /* Recommended */
    .test {
      display: block;
      height: 100px;
    }


Property Name Stops
-------------------
**Use a space after a property name's colon.**

Always use a single space between property and value (but no space between property and colon) for consistency reasons.

    /* Not recommended */
    h3 {
      font-weight:bold;
    }

    /* Recommended */
    h3 {
      font-weight: bold;
    }


Selector and Declaration Separation
-----------------------------------
**Separate selectors and declarations by new lines.**

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


Rule Separation
---------------
*\*In Flux** **Separate rules by new lines.**

Don't put a line between rules.

    /* Not recommended */
    html {
      background: #fff;
    }

    body {
      margin: auto;
      width: 50%;
    }

    /* Recommended */
    a {
      color: blue;
    }
    b {
      color: red;
    }

Section Comments
----------------
**Group sections by a section comment.**

If possible, group style sheets sections together by using comment headers. The headers should end with a dashed line out to the **80 character** rule. Additional documentation may be added below the header to further explain the significance of the section. Separate these sections with new lines.

    /* Header ---------------------------------------------- */

    .adw-header {}

    /* Footer ---------------------------------------------- */

    .adw-footer {}

    /* Gallery --------------------------------------------- */

    .adw-gallery {}

