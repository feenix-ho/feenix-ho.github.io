---
layout: post
title: Markdown Extended Syntax
categories:
- Tools and Tips
tags:
- markdown
toc: true
comments: true
math: true
mermaid: true
---
The [basic syntax]({% post_url 2023-03-31-markdown-basic-syntax %}) outlined in the original Markdown design document added many of the elements needed on a day-to-day basis, but it wasn’t enough for some people. That’s where extended syntax comes in.

Several individuals and organizations took it upon themselves to extend the basic syntax by adding additional elements like tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. These elements can be enabled by using a lightweight markup language that builds upon the basic Markdown syntax, or by adding an extension to a compatible Markdown processor.

## Availability

Not all Markdown applications support extended syntax elements. You’ll need to check whether or not the lightweight markup language your application is using supports the extended syntax elements you want to use. If it doesn’t, it may still be possible to enable extensions in your Markdown processor.

### Lightweight Markup Languages

There are several lightweight markup languages that are _supersets_ of Markdown. They include basic syntax and build upon it by adding additional elements like tables, code blocks, syntax highlighting, URL auto-linking, and footnotes. Many of the most popular Markdown applications use one of the following lightweight markup languages:

- [CommonMark](https://commonmark.org/)
- [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/)
- [Markdown Extra](https://michelf.ca/projects/php-markdown/extra/)
- [MultiMarkdown](https://fletcherpenney.net/multimarkdown/)
- [R Markdown](https://rmarkdown.rstudio.com/)

### Markdown Processors

There are [dozens of Markdown processors](https://github.com/markdown/markdown.github.com/wiki/Implementations) available. Many of them allow you to add extensions that enable extended syntax elements. Check your processor’s documentation for more information.

## Tables

To add a table, use three or more hyphens (<span style="font-family:courier">---</span>) to create each column’s header, and use pipes (<span style="font-family:courier">|</span>) to separate each column. For compatibility, you should also add a pipe on either end of the row.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
| Syntax      | Description |<br>
| ----------- | ----------- |<br>
| Header      | Title       |<br>
| Paragraph   | Text        |<br>
</p>

The rendered output looks like this:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

Cell widths can vary, as shown below. The rendered output will look the same.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
| Syntax | Description |<br>
| --- | ----------- |<br>
| Header | Title |<br>
| Paragraph | Text |<br>
</p>

{% include tip.html content="Creating tables with hyphens and pipes can be tedious. To speed up the process, try using the [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables) or [AnyWayData Markdown Export](https://anywaydata.com/). Build a table using the graphical interface, and then copy the generated Markdown-formatted text into your file." %}

### Alignment

You can align text in the columns to the left, right, or center by adding a colon (:) to the left, right, or on both side of the hyphens within the header row.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
| Syntax      | Description | Test Text     |<br>
| :---        |    :----:   |          ---: |<br>
| Header      | Title       | Here's this   |<br>
| Paragraph   | Text        | And more      |<br>
</p>

The rendered output looks like this:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text     |    And more |

### Formatting Text in Tables

You can format the text within tables. For example, you can add [links]({% post_url 2023-03-31-markdown-basic-syntax %}#links), [code]({% post_url 2023-03-31-markdown-basic-syntax %}#code) (words or phrases in backticks (<span style="font-family:courier">`</span>) only, not [code blocks]({% post_url 2023-03-31-markdown-basic-syntax %}#code-blocks)), and [emphasis]({% post_url 2023-03-31-markdown-basic-syntax %}#emphasis).

You can’t use headings, blockquotes, lists, horizontal rules, images, or most HTML tags.

{% include tip.html content="You can use HTML to create [line breaks]() and add [lists]() within table cells." %}

### Escaping Pipe Characters in Tables

You can display a pipe (<span style="font-family:courier">|</span>) character in a table by using its HTML character code (<span style="font-family:courier">&#38;#124;</span>).

## Fenced Code Blocks

The basic Markdown syntax allows you to create [code blocks]({% post_url 2023-03-31-markdown-basic-syntax %}#code-blocks) by indenting lines by four spaces or one tab. If you find that inconvenient, try using fenced code blocks. Depending on your Markdown processor or editor, you’ll use three backticks (<span style="font-family:courier">```</span>) or three tildes (<span style="font-family:courier">~~~</span>) on the lines before and after the code block. The best part? You don’t have to indent any lines!

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
```<br>
{<br>
  &nbsp;&nbsp;"firstName": "John",<br>
  &nbsp;&nbsp;"lastName": "Smith",<br>
  &nbsp;&nbsp;"age": 25<br>
}<br>
```
</p>

The rendered output looks like this:

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

<div markdown="span" class="alert alert-success" role="alert">
  <i class="fa fa-check-square-o"></i> <b>Tip:</b> Need to display backticks inside a code block? See <a href='{% post_url 2023-03-31-markdown-basic-syntax %}#escaping-backticks'>this section</a> to learn how to escape them.
</div>

### Syntax Highlighting

Many Markdown processors support syntax highlighting for fenced code blocks. This feature allows you to add color highlighting for whatever language your code was written in. To add syntax highlighting, specify a language next to the backticks before the fenced code block.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
```json<br>
{<br>
  &nbsp;&nbsp;"firstName": "John",<br>
  &nbsp;&nbsp;"lastName": "Smith",<br>
  &nbsp;&nbsp;"age": 25<br>
}<br>
```
</p>

The rendered output looks like this:

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## Footnotes

Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets (<span style="font-family:courier">[&#136;1]</span>). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text (<span style="font-family:courier">[&#136;1]: My footnote.</span>). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
Here's a simple footnote,[^1] and here's a longer one.[^bignote]<br>
<br>
[^1]: This is the first footnote.<br>
[^bignote]: Here's one with multiple paragraphs and code.<br>
<br>
  &nbsp;Indent paragraphs to include them in the footnote.<br>
<br>
  &nbsp;`{ my code }`<br>
<br>
  &nbsp;Add as many paragraphs as you like.
</p>

The rendered output looks like this:

Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.

## Heading IDs

Many Markdown processors support custom IDs for [headings]({% post_url 2023-03-31-markdown-basic-syntax %}#headings) — some Markdown processors automatically add them. Adding custom IDs allows you to link directly to headings and modify them with CSS. To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
### My Great Heading {#custom-id}
</p>

The HTML looks like this:

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
&lt;h3 id="custom-id">My Great Heading&lt;/h3>  
</p>

### Linking to Heading IDs

You can link to headings with custom IDs in the file by creating a [standard link]({% post_url 2023-03-31-markdown-basic-syntax %}#links) with a number sign (<span style="font-family:courier">#</span>) followed by the custom heading ID. These are commonly referred to as _anchor links_.

<table>
  <thead class="thead-light">
    <tr>
      <th>Markdown</th>
      <th>HTML</th>
      <th>Rendered Output</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">[Heading IDs](#heading-ids)</td>
      <td style="font-family:courier"> &lt;a href="#heading-ids"&gt;Heading IDs&lt;/a&gt;</td>
      <td><a href="#heading-ids">Heading IDs</a></td>
    </tr>
  </tbody>
</table>

Other websites can link to the heading by adding the custom heading ID to the full URL of the webpage (e.g, <span style="font-family:courier">&#91;Heading IDs&#93;({% post_url 2023-04-01-markdown-extended-syntax %}#heading-ids)</span>).

## Definition Lists

Some Markdown processors allow you to create definition lists of terms and their corresponding definitions. To create a definition list, type the term on the first line. On the next line, type a colon followed by a space and the definition.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
First Term<br>
: This is the definition of the first term.<br>
<br>
Second Term<br>
: This is one definition of the second term.<br>
: This is another definition of the second term.<br>
</p>

The HTML looks like this:

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
&lt;dl><br>
  &nbsp;&lt;dt>First Term&lt;/dt><br>
  &nbsp;&lt;dd>This is the definition of the first term.&lt;/dd><br>
  &nbsp;&lt;dt>Second Term&lt;/dt><br>
  &nbsp;&lt;dd>This is one definition of the second term.&lt;/dd><br>
  &nbsp;&lt;dd>This is another definition of the second term.&lt;/dd><br>
&lt;/dl><br>
</p>

The rendered output looks like this:

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

## Strikethrough

You can strikethrough words by putting a horizontal line through the center of them. The result looks ~~like this~~. This feature allows you to indicate that certain words are a mistake not meant for inclusion in the document. To strikethrough words, use two tilde symbols (<span style="font-family:courier">~~</span>) before and after the words.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
~~The world is flat.~~ We now know that the world is round.
</p>

The rendered output looks like this:

~~The world is flat.~~ We now know that the world is round.

## Task Lists

Task lists (also referred to as checklists and todo lists) allow you to create a list of items with checkboxes. In Markdown applications that support task lists, checkboxes will be displayed next to the content. To create a task list, add dashes (<span style="font-family:courier">-</span>) and brackets with a space (<span style="font-family:courier">[ ]</span>) in front of task list items. To select a checkbox, add an <span style="font-family:courier">x</span> in between the brackets (<span style="font-family:courier">[x]</span>).

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
- [x] Write the press release<br>
- [ ] Update the website<br>
- [ ] Contact the media<br>
</p>

The rendered output looks like this:

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## Emoji

There are two ways to add emoji to Markdown files: copy and paste the emoji into your Markdown-formatted text, or type emoji shortcodes.

### Copying and Pasting Emoji

In most cases, you can simply copy an emoji from a source like [Emojipedia](https://emojipedia.org/) and paste it into your document. Many Markdown applications will automatically display the emoji in the Markdown-formatted text. The HTML and PDF files you export from your Markdown application should display the emoji.

{% include tip.html content="If you're using a static site generator, make sure you [encode HTML pages as UTF-8](https://www.w3.org/International/tutorials/tutorial-char-enc/)." %}

### Using Emoji Shortcodes

Some Markdown applications allow you to insert emoji by typing emoji shortcodes. These begin and end with a colon and include the name of an emoji.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
Gone camping! :tent: Be back soon.<br>
<br>
That is so funny! :joy:
</p>

The rendered output looks like this:

Gone camping! ⛺ Be back soon.

That is so funny! 😂

{% include note.html content="You can use this [list of emoji shortcodes](https://gist.github.com/rxaviers/7360908), but keep in mind that emoji shortcodes vary from application to application. Refer to your Markdown application's documentation for more information." %}

## Highlight

This isn’t common, but some Markdown processors allow you to highlight text. The result looks <mark>like this</mark>. To highlight words, use two equal signs (<span style="font-family:courier">==</span>) before and after the words.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
I need to highlight these ==very important words==.
</p>

The rendered output looks like this:

I need to highlight these <mark>very important words</mark>.

Alternatively, if your Markdown application supports [HTML]({% post_url 2023-03-31-markdown-basic-syntax %}#html), you can use the mark HTML tag.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
I need to highlight these &lt;mark>very important words&lt;/mark>.
</p>

## Subscript

This isn’t common, but some Markdown processors allow you to use subscript to position one or more characters slightly below the normal line of type. To create a subscript, use one tilde symbol (<span style="font-family:courier">~</span>) before and after the characters.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
H~2~O
</p>

The rendered output looks like this:

H<sub>2</sub>O

{% include tip.html content="Be sure to test this in your Markdown application before using it. Some Markdown applications use one tilde symbol before and after words not for subscript, but for [strikethrough](#strikethrough)."%}

Alternatively, if your Markdown application supports HTML, you can use the <span style="font-family:courier">sub</span> [HTML]({% post_url 2023-03-31-markdown-basic-syntax %}#html) tag.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
H&lt;sub>2&lt;/sub>O
</p>

## Superscript

This isn’t common, but some Markdown processors allow you to use superscript to position one or more characters slightly above the normal line of type. To create a superscript, use one caret symbol (<span style="font-family:courier">^</span>) before and after the characters.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
X^2^
</p>

The rendered output looks like this:

X<sup>2</sup>

Alternatively, if your Markdown application supports HTML, you can use the <span style="font-family:courier">sup</span> [HTML]({% post_url 2023-03-31-markdown-basic-syntax %}#html) tag.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
X&lt;sup>2&lt;/sup>
</p>

## Automatic URL Linking

Many Markdown processors automatically turn URLs into links. That means if you type <span style="font-family:courier">http://www.example.com</span>, your Markdown processor will automatically turn it into a link even though you haven’t [used brackets]({% post_url 2023-03-31-markdown-basic-syntax %}#links).

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
http://www.example.com
</p>

The rendered output looks like this:

[http://www.example.com](http://www.example.com)

## Disabling Automatic URL Linking

If you don’t want a URL to be automatically linked, you can remove the link by [denoting the URL as code]({% post_url 2023-03-31-markdown-basic-syntax %}#code) with backticks.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
`http://www.example.com`
</p>

The rendered output looks like this:

`http://www.example.com`
