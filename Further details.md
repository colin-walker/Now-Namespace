# Further details

#### This is a place to document usage scenarios, updates, and comments on issues/discussions.

An RSS feed traditionally distributes the content (full or partial) of new items (posts, podcast episodes, etc.) and, consequently, acts as a notification system that the feed has been updated. A feed reader will poll the feed either manually, at intervals, or some kind of automated 'ping' can provide instant updates.

RSS is mature, reliable and extensible so is an ideal means of transmitting other information not normally associated with feeds.

The primary purpose of the 'now' namespace is to allow for the sharing of '/now page' style updates separately to post information.

**Intentions for use**

With the `<now:content>` element being required the intention is for a client to show the contents of an update. While a client might just display an indication that an update has been made, this is not how the namespace was originally intended to be used. There is, however, nothing to stop a client from doing whatever it wants with the information it receives.

**Extensibility**

The issue of extensibility [was raised](https://github.com/colin-walker/Now-Namespace/issues/1), more specifically when someone's /now information has multiple parts which should be treated as separate items.

An initial response is that `<now:content>` could act as/be replaced by a container for multiple `<now:item>` elements and the client would interpret this as appropriate. It could have either just a block of content or, perhaps, individual items with categories:

`<now:item category="currently">...</now:item>`  
`<now:item category="movies">...</now:item>`

A reader could then do what it wanted with that info based on the user's preferences.

This introduces an additional layer of complexity (the namespace was intended to be as simple as possible) but is an option. Comments/suggestions welcome on the [issue](https://github.com/colin-walker/Now-Namespace/issues/1).

This is all still very fluid.
