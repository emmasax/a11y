---
layout: post
title: "Quick tip: Create valid and accessible links"
description: "The `<a>` element is often cited as the main building block of the World Wide Web. It is used to create a link to other pages, to anchors within the same page, to other resources (such as a PDF) or to an email address."
author: emma_patricios
categories:
  - Quick Tips
further_reading:
  - url:
    title:
    source:
---

It is a simple element in use on almost every site on the web, however it can also be easy to create links that are not accessible to many people.

## Start with valid HTML

In order for an `<a>` to be valid HTML it must have:

* an `href` attribute: the location of the anchor, page or resource
* link content: text describing where the link is going, this could be plain text or an <a href="https://a11yproject.com/posts/alt-text/
">`alt`</a> attribute of an image
* opening and closing tags

## Write helpful link text

Link texts that are used quite often are 'click here', 'read more' and 'link'. These are problematic because when a person using a screen-reader is navigating using links these will be read out of context. Where would you expect any of those three links to go if you heard them? It's impossible to know.

Think about restructuring your sentence to remove 'click here' or 'link' then surround the meaningful part with the link:

```
To see our documentation <a href="/README.md">click here</a>. // bad

We have made our <a href="/README.md">documentation</a> available. // better
```

'Read more' can be fixed by adding what we will be reading more about:

```
<a href="/full-article">Read more</a>. // bad

<a href="/full-article">Read more - Accessible Landmarks</a> // better
```

## What about the `title` attribute?

The `title` attribute is not exposed by browsers in an accessible way meaning that keyboard and touch-only users can never see that information.

> If you want to hide content from mobile and tablet users as well as assistive tech users and keyboard only users, use the title attribute.
>
> <a href="https://developer.paciellogroup.com/blog/2010/11/using-the-html-title-attribute/
">Using the HTML title attribute - The Paciello Group</a>

Ultimately, do not use the `title` attribute on `<a>` elements.

## Focus state and keyboard

Some developers/designers see the focus outline of links as ugly and remove them.
People navigating using the keyboard require this focus state to keep track of where they are. Best practice is to <a href="https://a11yproject.com/posts/never-remove-css-outlines/">never remove CSS outlines</a> however there are accessible solutions to styling.

A link can be activated by pressing the <kbd>Enter</kbd> key, so be mindful

## When an `<a>` is not suitable

A link with no `href` and scripting attached via the `onclick` attribute or listeners. This is most likely doing an action on the same page, such as opening a menu or toggling content and as such should be replaced with the `<button>` element.
