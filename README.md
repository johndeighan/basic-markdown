Basic Markdown
==============

This document will teach you a basic subset of full
markdown syntax. The syntax described should display
correctly in virtually all implementations of
markdown, including all implementations of GFM
(GitHub Flavored Markdown)

Paragraphs
----------

A paragraph is a sequence of non-blank lines containing
text that is flush left, i.e. with no leading whitespace.
There should be a blank line both before and after the
paragraph. You should not worry about where lines break -
the text will be wrapped to the full width available.
It is advised that you set up your editor to automatically
strip any trailing whitespace. If you want to force a
break in the text, use a '\' character, then continue your
text on the next line, i.e. make the '\' the last character
on the line.

> NOTE: Do not allow any line to begin with a '-' or '*' character.
>       You can prevent this by moving text around between lines
>       since that will not affect the display of the text, which
>       will be automatically wrapped to the width available.

Headings
--------

You should be able to get by with only 2 levels of headings.
You can produce a top level heading by typing the text flush left,
then following it with a line containing at least 3 '=' characters
and no other characters. There can be more than one line of text,
though there is usually only one. Also, the number of '=' characters
on the last line is usually about the same as the width of the
longest text line. For example:

	This is a top level heading
	===========================

will render as:

<div>

This is a top level heading
===========================

</div>

