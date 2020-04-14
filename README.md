# Light Speed

An insanely fast and performance-based Zola theme, ported from [Light Speed Jekyll](https://github.com/bradleytaunt/lightspeed).

Some fun facts about the theme:

* Perfect score on Google's Lighthouse audit
* Only ~600 bytes of CSS
* No JavaScript

Demo: [quirky-perlman-34d0da.netlify.com](https://quirky-perlman-34d0da.netlify.com)

-----

## Contents

- [Installation](#installation)
- [Options](#options)
  - [Title](#title)
  - [Sass](#Sass)
  - [Footer menu](#footer-menu)
  - [Netlify](#netlify)
- [Original](#original)
- [License](#license)

## Installation
First download this theme to your `themes` directory:

```bash
$ cd themes
$ git clone https://github.com/carpetscheme/lightspeed.git
```
and then enable it in your `config.toml`:

```toml
theme = "lightspeed"
```

Posts should be placed directly in the `content` folder.

## Options

### Title
Set a title and description in the config to appear in the site header:

```toml
title = "Different strokes"
description = "for different folks"

```

### Sass

Styles are compiled from sass and imported inline to the header :zap:

You can overide the styles by enabling sass compilation in the config:

```toml
compile_sass = true
```

...and placing a replacement `style.scss` file in your sass folder.

### Footer-menu
Set a field in `extra` with a key of `footer_links`:

```toml
[extra]

footer_links = [
    {url = "$BASE_URL/about", name = "About"},
    {url = "$BASE_URL/rss.xml", name = "RSS"},
    {url = "https://google.com", name = "Google"},
]
```

If you put `$BASE_URL` in a url, it will automatically be replaced by the actual
site URL.

Create pages such as `$BASE_URL/about` by placing them in a subfolder of the content directory, and specifying the path in the frontmatter:

```toml
path = "about"
```

### Netlify

Deployed on netlify? Let people know in the footer by setting `netlify` in `extra` as `true`.

```toml
[extra]

netlify = true
```

## Original
This template is based on the Jekyll template [Light Speed Jekyll](https://github.com/bradleytaunt/lightspeed) by **Bradley Taunt**:

- <https://github.com/bradleytaunt>
- <https://twitter.com/bradtaunt>


## License

Open sourced under the [MIT license](LICENSE.md).

This project is open source except for example articles found in `content`.

