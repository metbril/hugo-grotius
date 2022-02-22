# Hugo Grotius

A personal theme for [Hugo][gohugo].

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<details>
<summary>Table of Contents</summary>

- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
  - [Site configuration](#site-configuration)
  - [Front matter](#front-matter)
- [IndieWeb Posts](#indieweb-posts)
  - [Sections](#sections)
  - [Localization](#localization)
- [Hugo Grotius???](#hugo-grotius)
- [Social icons](#social-icons)
- [Localization / Internationalization](#localization--internationalization)
- [Credits](#credits)

</details>
<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Features

- Internationalization en localization
- Social icons

## Installation

TODO

## Configuration

### Site configuration

TODO, see exampleSite config.toml

### Front matter

The theme supports some specific keys in content front matter.

Key | Description
--- | ---
`hidden:` | `true` or `false`. When `true`, hides the post from any range/list. This is useful to create pages that should be available by their permalink, but are not actively shown. If omitted, it will default to `false`.

### Localization

If you like to localize your post types, for example use 'bladwijzer' (Dutch) instead of 'bookmark', just create the section with that name, and add an `_index.md` file with some specific frontmatter.

The frontmatter in the index file should force the type and cascade it to all child pages:

Example file `/content/bladwijzer/_index.md`:

```yaml
type: bookmark
cascade:
  type: bookmark
```

## Social icons

The template has support for a user-defined set of social icons.
The icons are configured in the site configuration.
To add a spacer between 2 icons, just create an item without a url. Just an id will do.
You can use any available ForkAwesome icon.
See the configuration file in the example site.

Example file `data/social.yaml`:

```yaml
social:
  - id: twitter
    name: Twitter
    url: https://twitter.com/gohugoio
    icon: fa-twitter
    style: fab

  - id: github
    name: GitHub
    url: https://github.com/gohugoio
    icon: fa-github
    style: fab

  - id: spacer1

  - id: www
    name: "WWW"
    url: https://gohugo.io
    icon: fa-globe
    style: fas

  - id: email
    name: "E-mail"
    url: mailto:info@gohugo.io
    icon: fa-envelope
    style: fas
```

## Localization / Internationalization

The theme has official [i18n](https://gohugo.io/functions/i18n/) support.

To [customize dates](https://gohugo.io/content-management/multilingual/#customize-dates), the theme uses the `dateFormat` function, which outputs localized month names.

## Hugo Grotius???

[Hugo Grotius](https://en.wikipedia.org/wiki/Hugo_Grotius) (Hugo de Groot) is a Dutch historical figure.

## Credits

- [Normalize](https://necolas.github.io/normalize.css/) version 8.0.1
- [SimpleCSS](https://simplecss.org/) version 2.0.0
- [ForkAwesome](https://forkaweso.me/) version 1.2.0
- Wikimedia [picture of Hugo Grotius](https://commons.wikimedia.org/wiki/File:Michiel_Jansz_van_Mierevelt_-_Hugo_Grotius.jpg)

[gohugo]: https://gohugo.io/
[indieweb]: https://indieweb.org/
[hugo-sections]: https://gohugo.io/content-management/sections/
[hugo-content-type]: https://gohugo.io/content-management/types/
[iw-note]: https://indieweb.org/note
[iw-article]: https://indieweb.org/article
[iw-like]: https://indieweb.org/like
[iw-bookmark]: https://indieweb.org/nbookmark
