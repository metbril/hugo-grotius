# Hugo Grotius

A personal theme for [Hugo][gohugo] with [IndieWeb][indieweb] support.

## Features

- Indieweb
  - Post types
  - Author card / h-card
- Internationlization en localization
- Social icons

## Installation

TODO

## Configuration

### Site configuration

TODO

### Front matter

The theme supports some specific keys in content front matter.

Key | Description
--- | ---
`hidden:` | `true` or `false`. When `true`, hides the post from any range/list. This is useful to create pages that should be available by their permalink, but are not actively shown. If omitted, it will default to `false`.
`indieweb:` | Used for displaying IndieWeb post types. Supports multiple sub keys: `reply`, `like` and `bookmark`
`reply:` | Subkey for `indieweb`. Indicates an "in repy to". Has subkeys `link` and `title`.
`like:` | Subkey for `indieweb`. Indicates a "like of". Has subkeys `link` and `title`.
`bookmark:` | Subkey for `indieweb`. Indicates a "bookmark of". Has subkeys `link` and `title`.

## IndieWeb Posts

### Sections

The theme expects [IndieWeb posts](https://indieweb.org/posts) as separate root [sections][hugo-sections].

The advantage of this is, that the IndieWeb post type by default is determined by the root section the page is in. You don't need to explicitly set the Hugo [content type][hugo-content-type]. Post discovery is not required.

Another advantage is, that Hugo supports post type views out of the box. You can simply open a section/view and list all pages in it.

So your site will have sections like 'note', 'article', 'like' etc. These sections become Hugo content types. Layout templates in the theme are based on those content types.

These post types are currently supported:

- [note][iw-note]
- [article][iw-article]
- [like][iw-like]
- [bookmark][iw-bookmark]

Any unsupported type will fallback to the default layouts.

### Localization

If you like to localize your post types, for example use 'bladwijzer' (Dutch) instead of 'bookmark', just create the section with that name, and add an `_index.md` file with some specific frontmatter.

The frontmatter in the index file should force the type and cascade it to all child pages:

Example file `/content/bladwijzer/_index.md`:

```yaml
type: bookmark
cascade:
  type: bookmark
```

## Hugo Grotius???

[Hugo Grotius](https://en.wikipedia.org/wiki/Hugo_Grotius) (Hugo de Groot) is a Dutch historical figure.

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

## Credits

- [Normalize](https://necolas.github.io/normalize.css/) version 8.0.1
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
