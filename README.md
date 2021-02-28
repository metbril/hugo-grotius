# hugo-grotius
Hugo Grotius Theme

## IndieWeb Posts

### Sections

The theme expects [IndieWeb posts](https://indieweb.org/posts) as separate sections. The advantage is, that the post type is determined by the section the page is in. You don't need to explicitly set the type. Post discovery is not required. Another advantage is, that Hugo supports post type views out of the box. You can simply open a section/view and list all pages in it.

So your site will have sections like 'note', 'article', 'like' etc. These sections become Hugo page types. Layout templates in the theme are based on those layouts.

These post types are currently supported:

- note
- article
- like
- bookmark

Any unsupported type will fallback to the default layouts.

### Localization

If you like to localize your post types, for example use 'bladwijzer' (Dutch) instead of 'bookmark', just create the section with that name, and add an `_index.md` file with some specific frontmatter.

The frontmatter in the index file should force the type and cascade it to all child pages:

`/content/bladwijzer/_index.md`
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

Example file: `data/social.yaml`

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

To [customize dates](https://gohugo.io/content-management/multilingual/#customize-dates), a per language translation file is available in the `data` folder.

## Credits

- [Normalize](https://necolas.github.io/normalize.css/) version 8.0.1
- [FontAwesome](https://fontawesome.com) version 5.11.2
- Wikimedia [picture of Hugo Grotius](https://commons.wikimedia.org/wiki/File:Michiel_Jansz_van_Mierevelt_-_Hugo_Grotius.jpg)