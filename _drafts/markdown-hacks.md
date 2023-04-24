---
layout: post
title: Markdown Hacks
categories:
- Tools and Tips
tags:
- markdown
toc: true
comments: true
math: true
mermaid: true
---
The majority of people using Markdown will find that the [basic]() and [extended syntax]() elements cover their needs. But chances are that if you use Markdown long enough, you’ll inevitably discover that it doesn’t support something you need. This page provides tips and tricks for working around Markdown’s limitations.

{% include tip.html content="These hacks aren't guaranteed to work in your Markdown application. If you need to use these hacks frequently, you should consider writing using something other than Markdown." %}

## Underline

Underlined text is not something you typically see in web writing, probably because underlined text is nearly synonymous with links. However, if you’re writing a paper or a report, you may need the ability to underline words and phrases. A couple of applications like [Bear](https://bear.app/) and [Simplenote](https://simplenote.com/) provide support for underlining text, but Markdown doesn’t natively support underlining. If your Markdown processor supports [HTML]({% post_url 2023-03-31-markdown-basic-syntax %}#html), you can use the <span style="font-family:courier">ins</span> HTML tag to underline text in your document.

<p class="highlight" style="font-family:courier; padding-bottom:10px; padding-left:20px">
Some of these words &lt;ins>will be underlined&lt;/ins>.
</p>

The rendered output looks like this:

Some of these words <ins>will be underlined</ins>.
