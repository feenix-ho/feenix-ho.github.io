---
layout: post
title: Markdown Cheat Sheet
date: 2023-03-31 00:54 +0700
categories: [Tools and Tips]
tags: [markdown]
toc: true
comments: true
math: true
mermaid: true
---

This Markdown cheat sheet provides a quick overview of all the Markdown syntax elements. It can’t cover every edge case, so if you need more information about any of these elements, refer to the reference guides for [basic syntax]({% post_url 2023-03-31-markdown-basic-syntax %}) and [extended syntax]({% post_url 2023-04-01-markdown-extended-syntax %}).

## Basic Syntax

These are the elements outlined in John Gruber’s original design document. All Markdown applications support these elements.

<table>
  <thead class="thead-light">
    <tr>
      <th>Element </th>
      <th>Markdown Syntax </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#headings">Heading</a>
      </td>
      <td style="font-family:courier">
        # H1<br>## H2<br>### H3
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#bold">Bold</a>
      </td>
      <td style="font-family:courier">
        **bold text**
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#italic">Italic</a>
      </td>
      <td style="font-family:courier">
        *italicized text*
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#blockquotes">Blockquote</a>
      </td>
      <td style="font-family:courier">
        > blockquote
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#ordered-lists">Ordered List</a>
      </td>
      <td style="font-family:courier">
        1. First item<br>2. Second item<br>3. Third item
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#unordered-lists">Unordered List</a>
      </td>
      <td style="font-family:courier">
        - First item<br>- Second item<br>- Third item
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Code</a>
      </td>
      <td style="font-family:courier">
        `code`
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Horizontal Rule</a>
      </td>
      <td style="font-family:courier">
        ---
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Link</a>
      </td>
      <td style="font-family:courier">
        [title](https://www.example.com)
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Image</a>
      </td>
      <td style="font-family:courier">
        ![alt text](image.jpg)
      </td>
    </tr>
  </tbody>
</table>

## Extended Syntax

These elements extend the basic syntax by adding additional features. Not all Markdown applications support these elements.

<table>
  <thead class="thead-light">
    <tr>
      <th>Element </th>
      <th>Markdown Syntax </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="">Table</a>
      </td>
      <td style="font-family:courier">
        | Syntax | Description |<br>| --- | --- |<br>| Header | Title |<br>| Paragraph | Text |
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Fenced Code Block</a>
      </td>
      <td style="font-family:courier">
        ```<br>{<br><code>&nbsp;&nbsp;</code>"firstName": "John",<br> <code>&nbsp;&nbsp;</code>"lastName": "Smith",<br> <code>&nbsp;&nbsp;</code>"age": 25<br>}<br>```
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Footnote</a>
      </td>
      <td style="font-family:courier">
        Here's a sentence with a footnote. [^1]<br><br>[^1]: This is the footnote.
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Heading ID</a>
      </td>
      <td style="font-family:courier">
        ### My Great Heading {#custom-id}       
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Definition List</a>
      </td>
      <td style="font-family:courier">
        term<br>: definition 
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Strikethrough</a>
      </td>
      <td style="font-family:courier">
        ~~The world is flat.~~
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Task List</a>
      </td>
      <td style="font-family:courier">
        - [x] Write the press release<br>- [ ] Update the website<br>- [ ] Contact the media
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Emoji</a><br>(see also <a href="">Copying and Pasting Emoji</a>)
      </td>
      <td style="font-family:courier">
        That is so funny! :joy:
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Highlight</a>
      </td>
      <td style="font-family:courier">
        I need to highlight these ==very important words==.
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Subscript</a>
      </td>
      <td style="font-family:courier">
        H~2~O
      </td>
    </tr>
    <tr>
      <td>
        <a href="">Superscript</a>
      </td>
      <td style="font-family:courier">
        X^2^
      </td>
    </tr>

  </tbody>
</table>

## Downloads

You can [download this cheat sheet as a Markdown file](/assets/downloads/markdown-cheat-sheet.md) for use in your Markdown application.
