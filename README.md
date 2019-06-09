# hugo-purus: A pure theme for Hugo

*purus*&nbsp;(the Latin word for 'pure') is the theme powering [my personal website](https://bastian.rieck.me).
It offers you *the* no-frills experience for [Hugo](https://gohugo.io) that you might be craving for.

## Caveat emptor

I am new to Hugo and new to writing themes for it. If you think
something can be solved more generally or more elegantly, tell me!

## Summary

The theme is mean to support a simple&nbsp;(personal | academic) website with an additional blog section. It
assumes that the content is laid out in the following form in your `content` folder:

- `_index.md`: the main index file
- `foo.md`: a section called `foo`
- `bar.md`: a section called `bar`
- `blog/`: a folder containing your blog posts

## How to use

**Step 1:** Clone the repository into your local `themes` folder for Hugo. If you
are already using `git` to keep track of the changes of your website,
you should make this into a `submodule`. If you are not using `git`
already for this purpose, you really should start doing so.
Set `theme = "purus"` in your `config.toml`.

**Step 2:** Start adding menu entries to your configuration file `config.toml`. Here is an example from my own website:

```
[[menu.main]]
  name = "About"
  url  = "/about/"

[[menu.main]]
  name = "Blog"
  url = "/blog/"
  weight = -50

[[menu.main]]
  name = "Research"
  url  = "/research/"
  weight = -100
```

The `weight` parameter can be used to sort entries.

**Step 3:** Add footer information into `config.toml`. This is what will
be shown in the footer for *every* page. Again, here is a simple
example:

```
[params.footer]
  text = """
  This is a simple footer.
  You can use multiple lines and *markdown* commands.
"""
```

**Step 4**: Create awesome content! Nothing is pre-configured in this
theme except for an automated treatment of blog posts. If you blog,
create a file `_index.md` in a `blog` directory. This is the preamble or prefix for all your articles; they will just be added as a *list* to this page. My `_index.md` just contains a general introduction to my blog and a header `# All articles` to indicate the beginning of the list of articles. Strictly speaking, this is not required, though.

## Extras

I have not (yet) defined too many extra shortcodes anything, but you can
use `{{< tag_cloud >}}` in your content to create a tag cloud of blog
articles, for example.
