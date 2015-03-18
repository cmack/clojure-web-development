# Leiningen

## What is it?

In short, Clojures build tool. It can handle creating new projects from
templates, running tests, installing dependencies, starting up a REPL,
and so much more!

## How do I get it?

1. Download the [lein script](https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein) (or on Windows [lein.bat](https://raw.githubusercontent.com/technomancy/leiningen/stable/bin/lein.bat))

2. Place it on your `$PATH` where your shell can find it (eg. `~/bin`)

3. Set it to be executable (`chmod a+x ~/bin/lein`)

4. Run it (`lein`) and it will download the self-install package

## How do I start a REPL?

Just run `lein repl`. It's that simple!

## How do I create a new project?

`lein new [template name] [my project name]`

### How do I know what templates are available and what they do?

Right now there's no canonical list of templates with links to their source.
Fortunately it's still relatively easy to find templates and their source.

Lein actually pulls templates from one of several maven repositories. Lein
also comes with a convenient search task. You can simply search with
`lein search lein-template` and get a pretty good idea of what's out there.
You can find most templates on github under a similar name.

More often than not though you'll probably hear about useful templates through the
community and only use a small handful for most work (or even create your own).

**Note**: By default `lein search` only returns 50 results per page. You can request
a specific page by adding the page number as an argument to `lein search` like so:
`lein search lein-template 5`. You can also increase the number of results per
page by editing your `:user` profile and adding `:search-page-size [number I want here]`.
For more information about profiles see
[this lein wiki page](https://github.com/technomancy/leiningen/blob/master/doc/PROFILES.md)

## Can I extend lein?

**YES!** There's a somewhat canonical list of lein plugins
[here](https://github.com/technomancy/leiningen/wiki/Plugins). You install them
by adding them to your user profile. If you aren't sure how to do that check out
[this document](https://github.com/technomancy/leiningen/blob/master/doc/PROFILES.md).
