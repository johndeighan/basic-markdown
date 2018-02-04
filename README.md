Basic Markdown
==============

This document will teach you a basic subset of full
markdown syntax. The syntax described should display
correctly in virtually all implementations of
markdown, including all implementations of GFM
(GitHub flavored markdown).

> **NOTE:** In markdown, all text, except code blocks, should be
>           entered flush left. However, technically, you may
>           start a line with 1, 2 or 3 space characters, and they
>           will be ignored. This is really only useful for ordered
>           lists where you may prefer to make the periods in ' 1.'
>           and '10.' line up vertically.

Paragraphs
----------

A paragraph is a sequence of non-blank lines containing
text that is flush left, i.e. with no leading whitespace.
There should be a blank line both before and after the
paragraph. You should not worry about where lines break -
the text will be wrapped to the full width available.
It is advised that you set up your editor to automatically
strip any trailing whitespace. If you want to force a
break in the text, use a '\\' character, then continue your
text on the next line, i.e. make the '\\' the last character
on the line.

> NOTE: Do not allow any line to begin with a '-' or '*' character.
>       You can prevent this by moving text around between lines
>       since that will not affect the display of the text, which
>       will be automatically wrapped to the width available.

For example:

	This is a
	paragraph. It will automatically wrap
	when the text reaches the far right
	edge of the page - automatically. You
	do not need to concern yourself
	with where line endings occur.

will render as:

---------------------------------------

This is a
paragraph. It will automatically wrap
when the text reaches the far right
edge of the page - automatically. You
do not need to concern yourself
with where line endings occur.

---------------------------------------

Headings
--------

You should be able to get by with only 2 levels of headings.
You can produce a top level heading by typing the text flush
left, then following it with a line containing at least 3
'=' or '-' characters and no other characters. There can be
more than one line of text, though there is usually only
one. Also, the number of '=' or '-' characters on the last line
is usually about the same as the width of the longest text
line. I recommend always having a blank line before and after
any heading. For example:

	This is a top level heading
	===========================

will render as:

---------------------------------------

This is a top level heading
===========================

---------------------------------------

Also,

	This is a second level heading
	------------------------------

will render as:

---------------------------------------

This is a second level heading
------------------------------

---------------------------------------

> NOTE: There is a second style of heading in markdown which allows
>       you to have up to 6 levels of heading. However, I find it
>       less readable. If you need more than 2 levels of heading,
>       you can google "markdown" or "github flavored markdown"
>       to find out how to use it.

Code Blocks
-----------

Blocks of code are produced by taking any block of text, then adding
a leading TAB character to each line. Blank lines need not, and
should not, contain a TAB character (no lines should ever contain any
trailing whitespace, i.e. space or TAB characters). Here is an
example:

> NOTE: Because I'm using code blocks to display markdown source code,
>       the following 2 pieces of text are identical. Note, however,
>       that in the first piece, each non-blank line starts with a
>       TAB character.

	function sum(x, y) {

	return x + y;
	} // sum()

will render as:

---------------------------------------

	function sum(x, y) {

	return x + y;
	} // sum()

---------------------------------------

Lists
-----

Like HTML, in markdown there are 2 kinds of lists: ordered lists
and unordered lists. In an ordered list, each list item begins
with an integer, followed by a period, followed by a space character,
followed by any text you like. Each item should be flush left;
however, you may optionally include 1, 2 or 3 leading space
characters. This is useful, for example, to make the numbers line
up correctly if you have a mix of single digit, 2 digit and/or 3
digit numbers in the list. Only the number for the first item in the
list is actually used. After that, the displayed numbers will
increment by one for each item. This makes it very easy to insert
items in an ordered list - the numbers actually displayed will
automatically reorder themselves. Keep in mind, though, that
markdown is designed to be readable by itself, even if it isn't
rendered into HTML, so it's usually a good idea to fix the numbers
in the list when inserting or deleting list items.

As an example, this:

	1. apples
	2. oranges
	3. bananas

will render as:

---------------------------------------

1. apples
2. oranges
3. bananas

---------------------------------------

An unordered list can be constructed by having list items where
each item consists of a '-' character, followed by a space character,
followed by any desired text. For example, this:


	- apples
	- oranges
	- bananas

will render as:

---------------------------------------

- apples
- oranges
- bananas

---------------------------------------

> NOTE: Markdown lists are actually much more powerful than the
>       above simplified description. List items can be arbitrarily
>       long, but can be split in the markdown file. Also, lists
>       may have sublists, etc. For more information, google
>       'markdown' or 'github flavored markdown'.

Links
-----

A link is produced by having (flush left) the text that you wish
to be displayed with a '[' character before and a ']' character
after, followed by URL that the link leads to with a '(' character
before and a ')' character after. For example, this:

	Here is the [GFM specification](https://github.github.com/gfm/)!

will be rendered as:

---------------------------------------

Here is the [GFM specification](https://github.github.com/gfm/)!

---------------------------------------

Images
------

An image can be included in a markdown file by having a '!'
character, followed by the "alt text" for the image (which should
always be there for screen readers used by visually impaired
individuals) with a '[' character before and a ']' character
after, followed by URL of the image with a '(' character
before and a ')' character after. For example, this:

	![rappelling](https://scontent.fric1-2.fna.fbcdn.net/v/t31.0-8/16252041_10154124695520264_3803006618953557370_o.jpg?oh=2201e8287a123a5183179294344ff13d&oe=5AE6E5CD)

will be rendered as:

---------------------------------------

![rappelling](https://scontent.fric1-2.fna.fbcdn.net/v/t31.0-8/16252041_10154124695520264_3803006618953557370_o.jpg?oh=2201e8287a123a5183179294344ff13d&oe=5AE6E5CD)

---------------------------------------

Block Quote
-----------

