The AEO Front-end Dev Style Guide
=================================
***Working Draft***

Our agreed-upon guide for HTML, CSS, JS development style and practices. It aims at improving collaboration, code quality, and enabling supporting infrastructure. It applies to raw, working files that use HTML and CSS files. Tools are free to obfuscate, minify, and compile as long as the general code quality is maintained.

The General, HTML, and CSS guides (and some of this README) are forked/inspired from [Google's HTML/CSS guide](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml). The JS guide is TBD but may eventually start as a fork of [Idiomatic.js](https://github.com/rwldrn/idiomatic.js/).

This guide itself should be authored in [Markdown](http://daringfireball.net/projects/markdown/); as it currently lives on [GitHub](https://github.com/), you may also use [GitHub Flavored Markdown](http://github.github.com/github-flavored-markdown/).


### A Note on the Working Draft
Any rules that have yet to be reviewed or have not come to a team consensus will be labeled as *\*In Flux**. This label may only be temporary; all rules must be evaluated and finalized before terminating weekly discussions (despite any individual reservations). Any rule may be reevaluated again in the future, but should be accompanied by compelling and well-thought reasoning for the amendment.


Parting Words
-------------
Be consistent.

If you're editing code, take a few minutes to look at the code around you and determine its style. If they use spaces around all their arithmetic operators, you should too. If their comments have little boxes of hash marks around them, make your comments have little boxes of hash marks around them too.

The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you're saying rather than on how you're saying it. We present global style rules here so people know the vocabulary, but local style is also important. If code you add to a file looks drastically different from the existing code around it, it throws readers out of their rhythm when they go to read it. Avoid this.
