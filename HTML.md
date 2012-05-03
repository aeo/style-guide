HTML Style Rules
================

Document type
-------------
Use HTML5.
HTML5 (HTML syntax) is preferred for all HTML documents: <!DOCTYPE html>.

(It is recommended to use HTML, as text/html. Do not use XHTML. XHTML, as application/xhtml+xml, lacks both browser and infrastructure support and offers less room for optimization than HTML.)

HTML validity
-------------
Use valid HTML where possible.
Use valid HTML code unless that is not possible due to otherwise unattainable performance goals regarding file size.

Use tools such as the W3C HTML validator to test.

Using valid HTML is a measurable baseline quality attribute that contributes to learning about technical requirements and constraints, and that ensures proper HTML usage.

    <!-- Not recommended -->
    <title>Test</title>
    <article>This is only a test.
    <!-- Recommended -->
    <!DOCTYPE html>
    <meta charset="utf-8">
    <title>Test</title>
    <article>This is only a test.</article>

Semantics
---------
Use HTML according to its purpose.
Use elements (sometimes incorrectly called “tags”) for what they have been created for. For example, use heading elements for headings, p elements for paragraphs, a elements for anchors, etc.

Using HTML according to its purpose is important for accessibility, reuse, and code efficiency reasons.

    <!-- Not recommended -->
    <div onclick="goToRecommendations();">All recommendations</div>
    <!-- Recommended -->
    <a href="recommendations/">All recommendations</a>

Multimedia fallback
-------------------
Provide alternative contents for multimedia.
For multimedia, such as images, videos, animated objects via canvas, make sure to offer alternative access. For images that means use of meaningful alternative text (alt) and for video and audio transcripts and captions, if available.

Providing alternative contents is important for accessibility reasons: a blind user has few cues to tell what an image is about without @alt, and other users may have no way of understanding what video or audio contents are about either.

(For images whose alt attributes would introduce redundancy, and for images whose purpose is purely decorative which you cannot immediately use CSS for, use no alternative text, as in alt="".)

    <!-- Not recommended -->
    <img src="spreadsheet.png">
    <!-- Recommended -->
    <img src="spreadsheet.png" alt="Spreadsheet screenshot.">

Separation of concerns
----------------------

Separate structure from presentation from behavior.
Strictly keep structure (markup), presentation (styling), and behavior (scripting) apart, and try to keep the interaction between the three to an absolute minimum.

That is, make sure documents and templates contain only HTML and HTML that is solely serving structural purposes. Move everything presentational into style sheets, and everything behavioral into scripts.

In addition, keep the contact area as small as possible by linking as few style sheets and scripts as possible from documents and templates.

Separating structure from presentation from behavior is important for maintenance reasons. It is always more expensive to change HTML documents and templates than it is to update style sheets and scripts.

    <!-- Not recommended -->
    <!DOCTYPE html>
    <title>HTML sucks</title>
    <link rel="stylesheet" href="base.css" media="screen">
    <link rel="stylesheet" href="grid.css" media="screen">
    <link rel="stylesheet" href="print.css" media="print">
    <h1 style="font-size: 1em;">HTML sucks</h1>
    <p>I’ve read about this on a few sites but now I’m sure:
      <u>HTML is stupid!!1</u>
    <center>I can’t believe there’s no way to control the styling of
      my website without doing everything all over again!</center>
    <!-- Recommended -->
    <!DOCTYPE html>
    <title>My first CSS-only redesign</title>
    <link rel="stylesheet" href="default.css">
    <h1>My first CSS-only redesign</h1>
    <p>I’ve read about this on a few sites but today I’m actually
      doing it: separating concerns and avoiding anything in the HTML of
      my website that is presentational.
    <p>It’s awesome!

Entity references
-----------------

Do not use entity references.
There is no need to use entity references like &mdash;, &rdquo;, or &#x263a;, assuming the same encoding (UTF-8) is used for files and editors as well as among teams.

The only exceptions apply to characters with special meaning in HTML (like < and &) as well as control or “invisible” characters (like no-break spaces).

    <!-- Not recommended -->
    The currency symbol for the Euro is &ldquo;&eur;&rdquo;.
    <!-- Recommended -->
    The currency symbol for the Euro is “€”.

Closing tags
------------

All tags should be closed appropriately even if they are optional. Though there are file size savings and scannability benefits of leaving out optional tags, we've decided to support the IE7/8s of the world and continue with habits we've already all adhere to.

    <!-- Not recommended -->
    <!DOCTYPE html>
    <title>Where are my closing tags?</title>
    <p>Qed.
    <!-- Recommended -->
    <!DOCTYPE html>
    <html>
      <head>
        <title>I feel warm and wrapped up in these two tags.</title>
      </head>
      <body>
        <p>Sic.</p>
      </body>
    </html>


type attributes
---------------

Omit type attributes for style sheets and scripts.
Do not use type attributes for style sheets (unless not using CSS) and scripts (unless not using JavaScript).

Specifying type attributes in these contexts is not necessary as HTML5 implies text/css and text/javascript as defaults. This can be safely done even for older browsers.

    <!-- Not recommended -->
    <link rel="stylesheet" href="//www.google.com/css/maia.css"
      type="text/css">
    <!-- Recommended -->
    <link rel="stylesheet" href="//www.google.com/css/maia.css">
    <!-- Not recommended -->
    <script src="//www.google.com/js/gweb/analytics/autotrack.js"
      type="text/javascript"></script>
    <!-- Recommended -->
    <script src="//www.google.com/js/gweb/analytics/autotrack.js"></script>

HTML Formatting Rules
=====================

General formatting
------------------

Use a new line for every block, list, or table element, and indent every such child element.
Independent of the styling of an element (as CSS allows elements to assume a different role per display property), put every block, list, or table element on a new line.

Also, indent them if they are child elements of a block, list, or table element.

(If you run into issues around whitespace between list items it is acceptable to put all li elements in one line. A linter is encouraged to throw a warning instead of an error.)

    <blockquote>
      <p><em>Space</em>, the final frontier.</p>
    </blockquote>
    <ul>
      <li>Moe
      <li>Larry
      <li>Curly
    </ul>
    <table>
      <thead>
        <tr>
          <th scope="col">Income
          <th scope="col">Taxes
      <tbody>
        <tr>
          <td>$ 5.00
          <td>$ 4.50
    </table>
