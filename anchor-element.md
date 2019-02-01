# The <a> element

The `<a>` element can be used to create links to various  to an anchor within the same page, a separate web page, resource or email address.

In order to be valid HTML it must have:

* an `href` attribute - which is the location of the anchor, page or resource
* link content - something describing where the link is going e.g: plain text or an `alt` attribute of an image
* opening and closing tags

```
<a href="#first-section">First section</a>

<a href="/faq">Frequently asked questions</a>

<a href="/page-1"><img alt="Back to previous page" src="back-arrow.png" /></a>

<a href="mailto:me@here.com">Email me</a>
```

## Common questions relating to accessibility

### What's wrong with link text 'click here', 'read more', etc?

link text should make sense out of context

### Why don't you have a `title` attribute?

	focus state
	link with onclick no href best to be a button
	link behaviour must be accessible using keyboard enter key
