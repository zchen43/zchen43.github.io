Workflow
============
Write however you would like in Markdown.
You can see it live compiled in the VSCode preview.

Note how images can be inserted both from a HTML request or 
locally. 

Using Pandoc to convert the MD file into a self-contained HTML
file. The great advantage is you could take it to-go and be hosted on any web server you would like (e.g., university department). The CL templeate is below.

```bash
pandoc $title.md \
       --output=$title.html \
       --to=html5 \
       --css=./github.css \
       --highlight-style=kate \
       --self-contained
```

The generated HTML can be opened and viewed locally by any Browser. Whever you are happy with it, just do the regular Git add/commit/push workflow to Github. The html file can then be servred via https://zchen43.github.io/$title.html

It seems like Github could compile raw markdown as well!



Markdown CSS
============

This is a collection of stylesheets to use when converting Markdown text
to HTML format. Stylesheets have been tested to work with Pandoc, but
might also work with other converters that output fairly plain HTML.

To use one of the stylesheets, just unpack somewhere convenient, e.g.
`~/.local/share/markdown-css` and then do something like

```bash
pandoc foo.md \
       --output=foo.html \
       --to=html5 \
       --css=$HOME/.local/share/markdown-css/tufte.css \
       --highlight-style=haddock \
       --self-contained
```

**Preview:**
[github](https://otsaloma.io/pub/markdown-css-github.html)
[tufte](https://otsaloma.io/pub/markdown-css-tufte.html)

Included stylesheets originate from other projects, and have merely been
adapted to work with Markdown and Pandoc, and also styles of some
elements have been tweaked to suit the authors' use cases and personal
taste. Original files have been kept in the repository to be able to
review the changes and to merge changes in from upstream. Anyone looking
for a base for their own work is likely to be better off turning to the
original sources.

* `github.css` is from [github-markdown-css][1] by Sindre Sorhus,
  available under the MIT license.

* `tufte.css` and the font `et-book` are from [tufte-css][2] by Dave
  Liepmann and contributors, available under the MIT license.

[1]: https://github.com/sindresorhus/github-markdown-css
[2]: https://github.com/edwardtufte/tufte-css

Stylesheets are available under the MIT license, see the file
[`COPYING`](COPYING) for details.


![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

![GitHub Logo](./sheep.jpg)