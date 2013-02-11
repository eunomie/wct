# Web Comments Today

A new step in my ~~world domination plan~~ static web site/blog generator.

This allows to add comments in a static blog, using [Web Log Today][wlt].

## How?

The comment form is loaded inside an `iframe` in your blog. The comment is store in a git commit, in a specific repository. Each comment is in his own file, using this convention:

    _comments/<site url>/<post name>/xxx.md

xxx is the number of the comment, first is 001, second is 002, etc. Comments will be displayed in this order.

File content starts by a header, in YAML, sperated by `---` lines. Mandatory parameters are:

* title
* author
* website

In a near futur, a gravatar url will be added.

Following content is the comment, in plain text. This is an example:

    ---
    title: My first comment
    author: CrEv
    website: http://log.winsos.net
    ---
    Hey, this is the first comment!



[wlt]: https://github.com/CrEv/wlt
