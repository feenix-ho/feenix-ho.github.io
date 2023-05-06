---
layout: post
title: Markdown Basic Syntax
date: 2023-03-31 15:27 +0700
tags: [markdown]
categories: [Tools and Tips]
toc: true
comments: true
math: true
mermaid: true
---

Nearly all Markdown applications support the basic syntax outlined in the original Markdown design document. There are minor variations and discrepancies between Markdown processors — those are noted inline wherever possible.

## Headings

To create a heading, add number signs (<span style="font-family:courier">#</span>) in front of a word or phrase. The number of number signs you use should correspond to the heading level. For example, to create a heading level three (<span style="font-family:courier">&lt;h3&gt;</span>), use three number signs (e.g., <span style="font-family:courier">### My Header</span>).

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
      <td style="font-family:courier">
        # Heading level 1
      </td>
      <td style="font-family:courier">
        &lt;h1&gt;Heading level 1&lt;/h1&gt;
      </td>
      <td>
        <h1 data-toc-skip="">Heading level 1</h1>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        ## Heading level 2
      </td>
      <td style="font-family:courier">
        &lt;h2&gt;Heading level 2&lt;/h2&gt;
      </td>
      <td>
        <h2 data-toc-skip="">Heading level 2</h2>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        ### Heading level 3
      </td>
      <td style="font-family:courier">
        &lt;h3&gt;Heading level 3&lt;/h3&gt;
      </td>
      <td>
        <h3 data-toc-skip="">Heading level 3</h3>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        #### Heading level 4
      </td>
      <td style="font-family:courier">
        &lt;h4&gt;Heading level  4&lt;/h4&gt;
      </td>
      <td>
        <h4>Heading level 4</h4>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        ##### Heading level 5
      </td>
      <td style="font-family:courier">
        &lt;h5&gt;Heading level 5&lt;/h5&gt;
      </td>
      <td>
        <h5>Heading level 5</h5>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        ###### Heading level 6
      </td>
      <td style="font-family:courier">
        &lt;h6&gt;Heading level 6&lt;/h6&gt;
      </td>
      <td>
        <h6>Heading level 6</h6>
      </td>
    </tr>
  </tbody>
</table>

### Alternate Syntax

Alternatively, on the line below the text, add any number of <span style="font-family:courier">==</span> characters for heading level 1 or <span style="font-family:courier">--</span> characters for heading level 2.

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
      <td style="font-family:courier">
        Heading level 1
        <br/>
        ===============
      </td>
      <td style="font-family:courier">
        &lt;h1&gt;Heading level 1&lt;/h1&gt;
      </td>
      <td>
        <h1 data-toc-skip="">Heading level 1</h1>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        Heading level 2
        <br/>
        ---------------
      </td>
      <td style="font-family:courier">
        &lt;h2&gt;Heading level 2&lt;/h2&gt;
      </td>
      <td>
        <h2 data-toc-skip="">Heading level 2</h2>
      </td>
    </tr>
  </tbody>
</table>

### Heading Best Practices

Markdown applications don’t agree on how to handle a missing space between the number signs (<span style="font-family:courier">#</span>) and the heading name. For compatibility, always put a space between the number signs and the heading name.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
          # Here's a Heading
      </td>
      <td style="font-family:courier">
          #Here's a Heading
      </td>
    </tr>
  </tbody>
</table>

You should also put blank lines before and after a heading for compatibility.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
          Try to put a blank line before...
          <br/>
          <br/>
          # Heading
          <br/>
          <br/>
          ...and after a heading.
      </td>
      <td style="font-family:courier">
          Without blank lines, this might 
          <br>
          not look right.
          <br/>
          # Heading
          <br/>
          Don't do this!
      </td>
    </tr>
  </tbody>
</table>

## Paragraphs

To create paragraphs, use a blank line to separate one or more lines of text.

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
      <td style="font-family:courier">
        I really like using Markdown.
        <br>
        I think I'll use it to format
        <br>
        all of my documents from now on.
      </td>
      <td style="font-family:courier">
        &lt;p&gt;I really like using Markdown&lt;/p&gt;
        <br>
        &lt;p&gt;I think I'll use it to format all
        <br>
        of my documents from now on.&lt;/p&gt;
      </td>
      <td>
        I really like using Markdown.
        <br>
        I think I'll use it to format
        <br>
        all of my documents from now on.
      </td>
    </tr>
  </tbody>
</table>

### Paragraph Best Practices

Unless the [paragraph is in a list](#paragraphs-in-lists), don’t indent paragraphs with spaces or tabs.

{% include note.html content="If you need to indent paragraphs in the output, see the section on how to [indent (tab)]()." %}

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
        Don't put tabs or spaces in front 
        <br>
        of your paragraphs.
        <br>
        Keep lines left-aligned like this.
      </td>
      <td style="font-family:courier">
        &nbsp;&nbsp;&nbsp;&nbsp;
        This can result in unexpected 
        <br>
        formatting problems.
        <br>
        <br>
        &nbsp;&nbsp;
        Don't add tabs or spaces in 
        <br>
        front of paragraphs.
      </td>
    </tr>
  </tbody>
</table>

## Line Breaks

To create a line break or new line (<span style="font-family:courier">&lt;br&gt;</span>), end a line with two or more spaces, and then type return.

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
      <td style="font-family:courier">
        This is the first line.  
        <br>
        And this is the second line.	
      </td>
      <td style="font-family:courier">
        &lt;p&gt;This is the first line.&lt;/p&gt;&lt;br&gt;
        <br>
        &lt;p&gt;And this is the second line.&lt;/p&gt;
      </td>
      <td>
        This is the first line.
        <br>
        And this is the second line.
      </td>
    </tr>
  </tbody>
</table>

### Line Break Best Practices

You can use two or more spaces (commonly referred to as “trailing whitespace”) for line breaks in nearly every Markdown application, but it’s controversial. It’s hard to see trailing whitespace in an editor, and many people accidentally or intentionally put two spaces after every sentence. For this reason, you may want to use something other than trailing whitespace for line breaks. If your Markdown application [supports HTML](), you can use the <span style="font-family:courier">&lt;br&gt;</span> HTML tag.

For compatibility, use trailing white space or the <span style="font-family:courier">&lt;br&gt;</span> HTML tag at the end of the line.

There are two other options I don’t recommend using. CommonMark and a few other lightweight markup languages let you type a backslash (<span style="font-family:courier">\\</span>) at the end of the line, but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. And at least a couple lightweight markup languages don’t require anything at the end of the line — just type return and they’ll create a line break.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
        First line with two spaces after.  
        <br>
        And the next line.
        <br>
        <br>
        First line with the HTML tag after.&lt;br&gt;
        <br>
        And the next line.
      </td>
      <td style="font-family:courier">
        First line with a backslash after.\
        <br>
        And the next line.
        <br>
        <br>
        First line with nothing after.
        <br>
        And the next line.
      </td>
    </tr>
  </tbody>
</table>

## Emphasis

You can add emphasis by making text bold or italic.

### Bold

To bold text, add two asterisks or underscores before and after a word or phrase. To bold the middle of a word for emphasis, add two asterisks without spaces around the letters.

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
      <td style="font-family:courier">
        I just love **bold text**.	
      </td>
      <td style="font-family:courier">
        I just love &lt;/strong&gt;bold text&lt;/strong&gt;.
      </td>
      <td>
        I just love <strong>bold text</strong>.
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        I just love __bold text__.	
      </td>
      <td style="font-family:courier">
        I just love &lt;/strong&gt;bold text&lt;/strong&gt;.
      </td>
      <td>
        I just love <strong>bold text</strong>.
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        Love**is**bold
      </td>
      <td style="font-family:courier">
        Love&lt;/strong&gt;is&lt;/strong&gt;bold
      </td>
      <td>
        Love<strong>is</strong>bold
      </td>
    </tr>
  </tbody>
</table>

#### Bold Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold the middle of a word for emphasis.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
        Love**is**bold
      </td>
      <td style="font-family:courier">
        Love__is__bold
      </td>
    </tr>
  </tbody>
</table>

### Italic

To italicize text, add one asterisk or underscore before and after a word or phrase. To italicize the middle of a word for emphasis, add one asterisk without spaces around the letters.

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
      <td style="font-family:courier">
        Italicized text is the *cat's meow*.		
      </td>
      <td style="font-family:courier">
        Italicized text is the &lt;em&gt;cat's meow&lt;/em&gt;.	
      </td>
      <td>
        Italicized text is the <em>cat's meow</em>.	
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        Italicized text is the _cat's meow_.	
      </td>
      <td style="font-family:courier">
        Italicized text is the &lt;em&gt;cat's meow&lt;/em&gt;.
      </td>
      <td>
        Italicized text is the <em>cat's meow</em>.	
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
        A*cat*meow
      </td>
      <td style="font-family:courier">
        A&lt;/strong&gt;cat&lt;/strong&gt;meow
      </td>
      <td>
        A<em>cat</em>meow	
      </td>
    </tr>
  </tbody>
</table>

#### Italic Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to italicize the middle of a word for emphasis.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
        A*cat*meow	
      </td>
      <td style="font-family:courier">
        A_cat_meow
      </td>
    </tr>
  </tbody>
</table>

### Bold and Italic

To emphasize text with bold and italics at the same time, add three asterisks or underscores before and after a word or phrase. To bold and italicize the middle of a word for emphasis, add three asterisks without spaces around the letters.

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
      <td style="font-family:courier">This text is ***really important***.</td>
      <td style="font-family:courier">This text is &lt;em&gt;&lt;strong&gt;really important&lt;/strong&gt;&lt;/em&gt;.</td>
      <td>This text is <em><strong>really important</strong></em>.</td>
    </tr>
    <tr>
      <td style="font-family:courier">This text is ___really important___.</td>
      <td  style="font-family:courier">This text is &lt;em&gt;&lt;strong&gt;really important&lt;/strong&gt;&lt;/em&gt;.</td>
      <td>This text is <em><strong>really important</strong></em>.</td>
    </tr>
    <tr>
      <td style="font-family:courier">This text is __*really important*__.</td>
      <td style="font-family:courier">This text is &lt;em&gt;&lt;strong&gt;really important&lt;/strong&gt;&lt;/em&gt;.</td>
      <td>This text is <em><strong>really important</strong></em>.</td>
    </tr>
    <tr>
      <td style="font-family:courier">This text is **_really important_**.</td>
      <td style="font-family:courier">This text is &lt;em&gt;&lt;strong&gt;really important&lt;/strong&gt;&lt;/em&gt;.</td>
      <td>This text is <em><strong>really important</strong></em>.</td>
    </tr>
    <tr>
      <td style="font-family:courier">This is really***very***important text.</td>
      <td style="font-family:courier">This is really&lt;em&gt;&lt;strong&gt;very&lt;/strong&gt;&lt;/em&gt;important text.</td>
      <td>This is really<em><strong>very</strong></em>important text.</td>
    </tr>
  </tbody>
</table>

{% include note.html content="The order of the <span style='font-family:courier'>em</span> and <span style='font-family:courier'>strong</span> tags might be reversed depending on the Markdown processor you're using." %}

#### Bold and Italic Best Practices

Markdown applications don’t agree on how to handle underscores in the middle of a word. For compatibility, use asterisks to bold and italicize the middle of a word for emphasis.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
          This is really***very***important text.
      </td>
      <td style="font-family:courier">
          This is really___very___important text.
      </td>
    </tr>
  </tbody>
</table>

## Blockquotes

To create a blockquote, add a <span style='font-family:courier'>></span> in front of a paragraph.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  > Dorothy followed her through many of the beautiful rooms in her castle.
</p>

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.

### Blockquotes with Multiple Paragraphs

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  > Dorothy followed her through many of the beautiful rooms in her castle.
  <br>
  >
  <br>
  > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
</p>

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Nested Blockquotes

Blockquotes can be nested. Add a <span style='font-family:courier'>>></span> in front of the paragraph you want to nest.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  > Dorothy followed her through many of the beautiful rooms in her castle.
  <br>
  >
  <br>
  >> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
</p>

The rendered output looks like this:

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

### Blockquotes with Other Elements

Blockquotes can contain other Markdown formatted elements. Not all elements can be used — you’ll need to experiment to see which ones work.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  > #### The quarterly results look great!<br>
  ><br>
  > - Revenue was off the chart.<br>
  > - Profits were higher than ever.<br>
  ><br>
  >  *Everything* is going according to **plan**.<br>
</p>

The rendered output looks like this:

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>   _Everything_ is going according to **plan**.

### Blockquotes Best Practices

For compatibility, put blank lines before and after blockquotes.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
        Try to put a blank line before...<br><br>
        &gt; This is a blockquote<br><br>
        ...and after a blockquote.
      </td>
      <td style="font-family:courier">
        Without blank lines, this might not look right.<br>
        &gt; This is a blockquote<br>
        Don't do this!
      </td>
    </tr>
  </tbody>
</table>

## Lists

You can organize items into ordered and unordered lists.

### Ordered Lists

To create an ordered list, add line items with numbers followed by periods. The numbers don’t have to be in numerical order, but the list should start with the number one.

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
  <td style="font-family:courier">
        1. First item<br>
        2. Second item<br>
        3. Third item<br>
        4. Fourth item
      </code>
    </td>
    <td style="font-family:courier">
        &lt;ol&gt;<br>
          &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
          &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
          &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
          &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
        &lt;/ol&gt;
      </code>
    </td>
    <td>
      <ol>
        <li>First item</li>
        <li>Second item</li>
        <li>Third item</li>
        <li>Fourth item</li>
      </ol>
    </td>
    </tr>
    <tr>
    <td style="font-family:courier">
          1. First item<br>
          1. Second item<br>
          1. Third item<br>
          1. Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ol&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ol&gt;
      </td>
      <td>
        <ol>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
          <li>Fourth item</li>
        </ol>
      </td>
    </tr>
    <tr>
    <td style="font-family:courier">
          1. First item<br>
          8. Second item<br>
          3. Third item<br>
          5. Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ol&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ol&gt;
      </td>
      <td>
        <ol>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
          <li>Fourth item</li>
        </ol>
      </td>
    </tr>
    <tr>
    <td style="font-family:courier">
          1. First item<br>
          2. Second item<br>
          3. Third item<br>
          &nbsp;&nbsp;&nbsp;&nbsp;1. Indented item<br>
          &nbsp;&nbsp;&nbsp;&nbsp;2. Indented item<br>
          4. Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ol&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item<br>
              &nbsp;&nbsp;&nbsp;&nbsp;&lt;ol&gt;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&gt;Indented item&lt;/li&gt;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&gt;Indented item&lt;/li&gt;<br>
              &nbsp;&nbsp;&nbsp;&nbsp;&lt;/ol&gt;<br>
            &nbsp;&nbsp;&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ol&gt;
      </td>
      <td>
        <ol>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item
            <ol>
              <li>Indented item</li>
              <li>Indented item</li>
            </ol>
          </li>
          <li>Fourth item</li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>

#### Ordered List Best Practices

CommonMark and a few other lightweight markup languages let you use a parenthesis (<span style="font-family:courier">)</span>) as a delimiter (e.g., <span style="font-family:courier">1) First item</span>), but not all Markdown applications support this, so it isn’t a great option from a compatibility perspective. For compatibility, use periods only.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
          1. First item<br>
          2. Second item
      </td>
      <td style="font-family:courier">
          1) First item<br>
          2) Second item
      </td>
    </tr>
  </tbody>
</table>

### Unordered Lists

To create an unordered list, add dashes <span style="font-family:courier">-</span> asterisks (<span style="font-family:courier">\*</span>), or plus signs (<span style="font-family:courier">+</span>) in front of line items. Indent one or more items to create a nested list.

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
      <td style="font-family:courier">
          - First item<br>
          - Second item<br>
          - Third item<br>
          - Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
      <td>
        <ul>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
          <li>Fourth item</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
          * First item<br>
          * Second item<br>
          * Third item<br>
          * Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
      <td>
        <ul>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
          <li>Fourth item</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
          + First item<br>
          + Second item<br>
          + Third item<br>
          + Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
      <td>
        <ul>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item</li>
          <li>Fourth item</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="font-family:courier">
          - First item<br>
          - Second item<br>
          - Third item<br>
          &nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>
          &nbsp;&nbsp;&nbsp;&nbsp;- Indented item<br>
          - Fourth item
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;First item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Second item&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Third item<br>
              &nbsp;&nbsp;&nbsp;&nbsp;&lt;ul&gt;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&gt;Indented item&lt;/li&gt;<br>
                &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;li&gt;Indented item&lt;/li&gt;<br>
              &nbsp;&nbsp;&nbsp;&nbsp;&lt;/ul&gt;<br>
            &nbsp;&nbsp;&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;Fourth item&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
      <td>
        <ul>
          <li>First item</li>
          <li>Second item</li>
          <li>Third item
            <ul>
              <li>Indented item</li>
              <li>Indented item</li>
            </ul>
          </li>
          <li>Fourth item</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Starting Unordered List Items With Numbers

If you need to start an unordered list item with a number followed by a period, you can use a backslash (<span style="font-family:courier">\</span>) to [escape]() the period.

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
      <td style="font-family:courier">
          - 1968\. A great year!<br>
          - I think 1969 was second best.
      </td>
      <td style="font-family:courier">
          &lt;ul&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;1968. A great year!&lt;/li&gt;<br>
            &nbsp;&nbsp;&lt;li&gt;I think 1969 was second best.&lt;/li&gt;<br>
          &lt;/ul&gt;
      </td>
      <td>
        <ul>
          <li>1968. A great year!</li>
          <li>I think 1969 was second best.</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Unordered List Best Practices

Markdown applications don’t agree on how to handle different delimiters in the same list. For compatibility, don’t mix and match delimiters in the same list — pick one and stick with it.

<table>
  <thead class="thead-light">
    <tr>
      <th>✅&nbsp; Do this</th>
      <th>❌&nbsp; Don't do this</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="font-family:courier">
          - First item<br>
          - Second item<br>
          - Third item<br>
          - Fourth item
      </td>
      <td style="font-family:courier">
          + First item<br>
          * Second item<br>
          - Third item<br>
          + Fourth item
      </td>
    </tr>
  </tbody>
</table>

### Adding Elements in Lists

To add another element in a list while preserving the continuity of the list, indent the element four spaces or one tab, as shown in the following examples.

{% include tip.html content="If things don't appear the way you expect, double check that you've indented the elements in the list four spaces or one tab." %}

#### Paragraphs {#paragraphs-in-lists}

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  * This is the first list item.<br>
  * Here's the second list item.<br>
  <br>
      &nbsp;&nbsp;&nbsp;&nbsp;I need to add another paragraph below the second list item.<br>
  <br>
  * And here's the third list item.<br>
</p>

The rendered output looks like this:

- This is the first list item.
- Here's the second list item.

  I need to add another paragraph below the second list item.

- And here's the third list item.

#### Blockquotes {#blockquotes-in-lists}

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  * This is the first list item.<br>
  * Here's the second list item.<br>
  <br>
      &nbsp;&nbsp;&nbsp;&nbsp;> A blockquote would look great below the second list item.<br>
  <br>
  * And here's the third list item.<br>
</p>

- This is the first list item.
- Here's the second list item.

  > A blockquote would look great below the second list item.

- And here's the third list item.

#### Code Blocks {#code-blocks-in-lists}

[Code blocks]() are normally indented four spaces or one tab. When they’re in a list, indent them eight spaces or two tabs.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  1.  Open the file.<br>
  2.  Find the following code block on line 21:<br>
  <br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;html&gt;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;head&gt;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;Test&lt;/title&gt;<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/head&gt;<br>
  <br>
  3.  Update the title to match the name of your website.
</p>

The rendered output looks like this:

1.  Open the file.
2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.

#### Images {#images-in-lists}

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  1. Open the file containing the Linux mascot.<br>
  2. Marvel at its beauty.<br>
  <br>
      &nbsp;&nbsp;![Tux, the Linux mascot](/assets/img/2023-03-31-markdown-basic-syntax/tux.jpg)<br>
  <br>
  3. Close the file.
</p>

1.  Open the file containing the Linux mascot.
2.  Marvel at its beauty.

    <img src='/assets/img/2023-03-31-markdown-basic-syntax/tux.jpg' alt='Tux, the Linux mascot' width=300>

3.  Close the file.

#### Lists {#lists-in-lists}

You can nest an unordered list in an ordered list, or vice versa.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
  1. First item<br>
  2. Second item<br>
  <br>
      &nbsp;&nbsp;- Indented item<br>
      &nbsp;&nbsp;- Indented item<br>
  <br>
  3. Third item<br>
</p>

1. First item
2. Second item

   - Indented item
   - Indented item

3. Third item

## Code

To denote a word or phrase as code, enclose it in backticks (<span style='font-family:courier'>`</span>).

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
      <td style='font-family:courier'>At the command prompt, type `nano`.</td>
      <td style='font-family:courier'>At the command prompt, type &lt;code&gt;nano&lt;/code&gt;. </td>
      <td>At the command prompt, type <code>nano</code>.</td>
    </tr>
  </tbody>
</table>

### Escaping Backticks

If the word or phrase you want to denote as code includes one or more backticks, you can escape it by enclosing the word or phrase in double backticks (<span style='font-family:courier'>``</span>).

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
      <td style='font-family:courier'>``Use `code` in your Markdown file.``</td>
      <td style='font-family:courier'>&lt;code&gt;Use `code` in your Markdown file.&lt;/code&gt;</td>
      <td><code>Use `code` in your Markdown file.</code></td>
    </tr>
  </tbody>
</table>
