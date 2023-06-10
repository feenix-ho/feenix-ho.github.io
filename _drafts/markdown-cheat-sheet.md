---
layout: post
title: Markdown Cheat Sheet
categories: [Tools and Tips]
tags: [markdown]
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
      <th>Markdown Syntax</th>
      <th>HTML Syntax</th>
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
      <td style="font-family:courier">
        &lt;h1>H1&lt;/h1><br>
        &lt;h2>H2&lt;/h2><br>
        &lt;h3>H3&lt;/h3><br>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#bold">Bold</a>
      </td>
      <td style="font-family:courier">
        **bold text**
      </td>
      <td style="font-family:courier">
        &lt;strong>bold text&lt;/strong>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#italic">Italic</a>
      </td>
      <td style="font-family:courier">
        *italicized text*
      </td>
      <td style="font-family:courier">
        &lt;em>italicized text&lt;/em>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#blockquotes">Blockquote</a>
      </td>
      <td style="font-family:courier">
        > blockquote
      </td>
      <td style="font-family:courier">
        &lt;blockquote><br>
        &nbsp;&nbsp;&lt;p>blockquote&lt;/p><br>
        &lt;/blockquote>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#ordered-lists">Ordered List</a>
      </td>
      <td style="font-family:courier">
        1. First item<br>2. Second item<br>3. Third item
      </td>
      <td style="font-family:courier">
          &lt;ol&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
          &lt;/ol&gt;
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#unordered-lists">Unordered List</a>
      </td>
      <td style="font-family:courier">
        - First item<br>- Second item<br>- Third item
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#code">Code</a>
      </td>
      <td style="font-family:courier">
        `code`
      </td>
      <td style='font-family:courier'>
        &lt;code&gt;nano&lt;/code&gt;
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#horizontal-rules">Horizontal Rule</a>
      </td>
      <td style="font-family:courier">
        ---
      </td>
      <td style='font-family:courier'>
        &lt;hr&gt;
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#links">Link</a>
      </td>
      <td style="font-family:courier">
        [title](https://www.example.com)
      </td>
      <td style='font-family:courier'>
        &lt;a href="https://www.example.com">title&lt;/a>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-03-31-markdown-basic-syntax %}#images">Image</a>
      </td>
      <td style="font-family:courier">
        ![alt text](image.jpg)
      </td>
      <td style="font-family:courier">
        &lt;img src="image.jpg">
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
      <th>HTML Syntax </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#tables">Table</a>
      </td>
      <td style="font-family:courier">
        | Syntax | Description |<br>| --- | --- |<br>| Header | Title |<br>| Paragraph | Text |
      </td>
      <td style="font-family:courier">
        &lt;table><br>
          &lt;thead><br>
            &lt;tr><br>
              &lt;th>Syntax&lt;/th><br>
              &lt;th>Description&lt;/th><br>
            &lt;/tr><br>
          &lt;/thead><br>
          &lt;tbody><br>
            &lt;tr><br>
              &lt;td>Header&lt;/td><br>
              &lt;td>Title&lt;/td><br>
            &lt;/tr><br>
            &lt;tr><br>
              &lt;td>Paragraph&lt;/td><br>
              &lt;td>Text&lt;/td><br>
            &lt;/tr><br>
          &lt;/tbody><br>
      &lt;/table><br>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#fenced-code-blocks">Fenced Code Block</a>
      </td>
      <td style="font-family:courier">
        ```<br>{<br><code>&nbsp;&nbsp;</code>"firstName": "John",<br> <code>&nbsp;&nbsp;</code>"lastName": "Smith",<br> <code>&nbsp;&nbsp;</code>"age": 25<br>}<br>```
      </td>
      <td style="font-family:courier">
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#footnotes">Footnote</a>
      </td>
      <td style="font-family:courier">
        Here's a sentence with a footnote. [^1]<br><br>[^1]: This is the footnote.
      </td>
      <td style="font-family:courier">
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}">Heading ID</a>
      </td>
      <td style="font-family:courier">
        ### My Great Heading {#custom-id}       
      </td>
      <td style="font-family:courier">
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#definition-lists">Definition List</a>
      </td>
      <td style="font-family:courier">
        term<br>: definition 
      </td>
      <td style="font-family:courier">
        &lt;dl><br>
          &nbsp;&lt;dt>term&lt;/dt><br>
          &nbsp;&lt;dd>definition&lt;/dd><br>
        &lt;/dl><br>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#strikethrough">Strikethrough</a>
      </td>
      <td style="font-family:courier">
        ~~The world is flat.~~
      </td>
      <td style="font-family:courier">
        &lt;del>The world is flat.&lt;/del>
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#task-lists">Task List</a>
      </td>
      <td style="font-family:courier">
        - [x] Write the press release<br>- [ ] Update the website<br>- [ ] Contact the media
      </td>
      <td style="font-family:courier">
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#emoji">Emoji</a><br>(see also <a href="">Copying and Pasting Emoji</a>)
      </td>
      <td style="font-family:courier">
        That is so funny! :joy:
      </td>
      <td style="font-family:courier">
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#highlight">Highlight</a>
      </td>
      <td style="font-family:courier">
        Highlight these ==important words==.
      </td>
      <td style="font-family:courier">
        Highlight these &lt;mark>important words&lt;/mark>.
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#subscript">Subscript</a>
      </td>
      <td style="font-family:courier">
        H~2~O
      </td>
      <td style="font-family:courier">
        H&lt;sub>2&lt;/sub>O
      </td>
    </tr>
    <tr>
      <td>
        <a href="{% post_url 2023-04-01-markdown-extended-syntax %}#superscript">Superscript</a>
      </td>
      <td style="font-family:courier">
        X^2^
      </td>
      <td style="font-family:courier">
        X&lt;sup>2&lt;/sup>
      </td>
    </tr>

  </tbody>
</table>

## Downloads

You can [download this cheat sheet as a Markdown file](/assets/downloads/markdown-cheat-sheet.md) for use in your Markdown application.
