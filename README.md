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

> **NOTE:** Do not allow any line to begin with a '-' or '*' character.
>           You can prevent this by moving text around between lines
>           since that will not affect the display of the text, which
>           will be automatically wrapped to the width available.

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

> **NOTE:** There is a second style of heading in markdown which allows
>           you to have up to 6 levels of heading. However, I find it
>           less readable. If you need more than 2 levels of heading,
>           you can google "markdown" or "github flavored markdown"
>           to find out how to use it.

Code Blocks
-----------

Blocks of code are produced by taking any block of text, then adding
a leading TAB character to each line. Blank lines need not, and
should not, contain a TAB character (no lines should ever contain any
trailing whitespace, i.e. space or TAB characters). Here is an
example:

> **NOTE:** Because I'm using code blocks to display markdown source code,
>           the following 2 pieces of text are identical. Note, however,
>           that in the first piece, each non-blank line starts with a
>           TAB character.

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

> **NOTE:** Markdown lists are actually much more powerful than the
>           above simplified description. List items can be arbitrarily
>           long, but can be split in the markdown file. Also, lists
>           may have sublists, etc. For more information, google
>           'markdown' or 'github flavored markdown'.

Task Lists
----------

Task lists are an extension to the original markdown spec and are
included in GitHub flavored markdown. They allow you to have an
unordered list where each item is preceded by a checkbox, which may be
checked or unchecked. Each item in a task list should begin with a '-'
character, followed by a space character, followed by a '[' character,
followed by either a space character (for an unchecked checkbox) or an
'x' character (for a checked checkbox), followed by a ']' character,
followed by a space character, followed by the text of the item.
For example, this:

	- [x] task 1
	- [ ] task 2
	- [x] task 3

will be rendered as:

---------------------------------------

- [x] task 1
- [ ] task 2
- [x] task 3

---------------------------------------

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

A block quote is like a paragraph, i.e. a sequence of non-blank
lines, except that each line begins with a '>' character,
followed by a space character. Block quotes are what is used
in this document to display "Notes". For example, this:

	> This is a
	> block quote which contains
	> enough text that it illustrates
	> that, like a paragraph, the
	> text in the block quote will be
	> displayed joined, then wrapped
	> at the right edge of the page.

will be rendered as:

---------------------------------------

> This is a
> block quote which contains
> enough text that it illustrates
> that, like a paragraph, the
> text in the block quote will be
> displayed joined, then wrapped
> at the right edge of the page.

---------------------------------------

Horizontal Rule
---------------

A horizontal rule, aka "thematic break" is produced by a line
containing 3 or more '-' characters and nothing else.
In this document, the rendering of markdown structures is
displayed with horizontal rules before and after the
rendered item. A horizontal rule looks like this:

---------------------------------------

Inline formatting
-----------------

Within the text of a paragraph, list item, block quote, etc.
(but not a code block, where text is taken literally)
you may apply formatting to words, phrases or other text.

To format text as inline code, surround the text with backticks:

	Enter the command `rmdir -R` to recursively remove a directory


will render as:

---------------------------------------

Enter the command `rmdir -R` to recursively remove a directory

---------------------------------------

> **NOTE:** If the text being rendered as inline code contains
>           single backtick characters, you may begin and end
>           the rendering with double backticks.

To format text as boldface text, use double asterisks:

	This is a **really important** step!

will render as:

---------------------------------------

This is a **really important** step!

---------------------------------------

(This was mentioned previously) To force a linebreak at a
particular position in the text, insert a '\\' character,
then start a new line:

	To be or not to be,\
	That is the question

will render as:

---------------------------------------

To be or not to be,\
That is the question

---------------------------------------

To render text with "strikethrough" characters, surround the
text with'~' characters:

	This can be done ~more~ better!

will render as:

---------------------------------------

This can be done ~more~ better!

---------------------------------------

To remove the special markdown meaning of a character, you can
escape the character with a preceding '\\' character:

	To boldface the word maximum, use \*\*maximum\*\*

will render as:

---------------------------------------

To boldface the word maximum, use \*\*maximum\*\*

---------------------------------------

You can use HTML character entities, though they're rarely required:

	Basic&copy; Markdown

will render as:

---------------------------------------

Basic&copy; Markdown

---------------------------------------

HTML
----

You can actually include HTML directly in your document and it
will output the HTML, which will render the way HTML normally
renders. However, you should be aware that GitHub performs
sanitation on your HTML, stripping out any JavaScript code and
even any CSS styles or classes, so it's virtually impossible to
affect the styling of your code. Also, in most cases, a blank
line will end any block of HTML that you insert, so if text
follows, it will be treated as markdown. This can be useful
for rendering tables or definition lists. For example:

	<table border="1">
	<tr>
	<td>

	Found in **China**

	</td>
	<td>

	1. A hole in a mountain
	5. Tibetan prayer flags

	</td>
	</tr>
	</table>

will be rendered as:

---------------------------------------

<table border="1">
<tr>
<td>

Found in **China**

</td>
<td>

1. A hole in a mountain
5. Tibetan prayer flags

</td>
</tr>
</table>

---------------------------------------

> **NOTE:** In the above markdown code, there are
>           exactly 3 blocks of HTML code.
>           Between them, there are 2 blocks of
>           markdown code.
