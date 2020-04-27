# Pickles
Pickles is a clean, responsive blog theme based on the Hugo theme with the same name featuring pagination.

![pickles screenshot](https://github.com/lukehsiao/zola-pickles/blob/master/screenshot.png?raw=true)

## Installation
First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/lukehsiao/zola-pickles.git
```
and then enable it in your `config.toml`:

```toml
theme = "zola-pickles"
```

The theme requires putting the posts in the root of the `content` folder and to
enable pagination, for example in `content/_index.md`:

```
+++
paginate_by = 5
sort_by = "date"
insert_anchor_links = "right"
+++
```

## Options

```toml
[extra]
# A line to display underneath the main title
subtitle = "Example subtitle"

# Text to display in the footer of the page
copyright = "Copyright authors year"

# Your Google Analytics ID
analytics = ""

# See below
katex_enable = false

# See below
instantpage_enable = false
```

A full example configuration is included in config.toml.

### KaTeX math formula support

This theme contains math formula support using [KaTeX](https://katex.org/),
which can be enabled by setting `katex_enable = true` in the `extra` section
of `config.toml`.

After enabling this extension, the `katex` short code can be used in documents:
* `{% katex(block=true) %}\KaTeX{% end %}` to typeset a block of math formulas,
  similar to `$$...$$` in LaTeX

### Figure Shortcode

This them also includes a figure shortcode for convenience in captioning figures.

```
{% figure(link="https://www.example.com/", src="https://www.example.com/img.jpeg", alt="sample alt text") %}
Your caption here.
{% end %}
```

### Fontawesome

This theme includes fontawesome, so that fontawesome icons can be directly used.

### Instant.page

The theme contains instant.page prefetching. This can be enabled by setting
`instantpage_enable = true` in the `extra` section of `config.toml`.
