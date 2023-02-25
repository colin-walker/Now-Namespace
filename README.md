# Now-Namespace
Description of the 'Now' RSS namespace

## About

The 'now' namespace is intended to allow for the sharing of updates via RSS that do not relate to traditional items, e.g. blog posts or podcast episodes. It takes it's name from the [/now page concept](https://nownownow.com/about) created by Derek Sivers.

The namespace will allow for additional channel level elements to share updates similar to the contents of a now page.

This is an initial version of the 'now' namespace - published 24th Jan 2023. The namespace lives [here](https://nowns.work) and that should serve as the namespace URI:

`xmlns:now="https://nowns.work"`

### Example feeds

- [colinwalker.blog](https://colinwalker.blog/livefeed.xml)
- [hyblog demo site](https://colinwalker.me.uk/hyblog.xml)

### now:title

An optional channel level element that provides the title for the update. It has no attributes and is simply stated as below:

`<now:title>Now Title</now:title>`

### now:link

An optional channel level element that provides the link to a /now page or other source of updates. It has no attributes and just contains a URL:

`<now:link>https://colinwalker.blog/now/</now:link>`

### now:content

A mandatory channel level element the holds the content for the update. This will operate in a similar manner to the standard RSS Description item element or the <code>content:encoded</code> extension. The content can be plain text or contain HTML etc. in a CDATA block:

`<now:content>I am writing the 'now' namespace documentation.</now:content>`

`<now:content><![CDATA[<p>I am writing the 'now' namespace documentation.</p>]]></now:content>`

### now:markdown

An optional channel level element that holds the content for the update but in markdown. This behaves in the same way as [`source:markdown`](http://source.scripting.com/#1653758422000) from the 'source' namespace.

`<now:markdown>I am writing the **'now'** namespace documentation.</now:markdown>`

### now:timestamp

An optional channel level element that specifies the date the update was published. This will operate in the same way as the RSS pubDate element and must conform to [RFC 822](https://www.w3.org/Protocols/rfc822/#z28) 

`<now:timestamp>Tue, 24 Jan 2023 00:00:04 GMT</now:timestamp>`

----

Check out [Further details](https://github.com/colin-walker/Now-Namespace/blob/main/Further%20details.md) for more info and discussion.
