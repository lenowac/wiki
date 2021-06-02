# Building a Markdown knowledge base

I've got a pile of Markdown files id like to form into a working knowledge base without too much effort.

## Github pages and Jekyll themes

all of them are bloated, but those seem to be the best:

### Just the Docs

modern, highly customizable, and responsive with search.
[Link](https://github.com/pmarsceill/just-the-docs)

### Help Center

Simple and responsive Jekyll theme for help center.
[Link](https://github.com/gustavoquinalha/jekyll-help-center-theme)

But, to be honest, all of them suck. Another alternative:

## Gatsby

...can really do anything. With some digging, I think I found the [holy grale](https://gatsby-project-kb.vercel.app/), the perfect personal knnowledge base theme.

### Setup

The initial setup went well, thanks to the docs. But for HOURS I kept getting errors. With lots of testing what kind of things are allowed in markdown, I managed to narrow it down to `<br>`, which (if used), breaks everything, because there's no closing statement. `<br/>` Works fine, just as well as `<br></br>`. Now I imagine it will be the same for `<hr>`. Besides that, you can really throw anything in there.

Something to keep in mind: you NEED a title. So files without a `title: ` prematter or `<h1>` or `#` will produce errors.