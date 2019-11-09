# hugo-grotius
Hugo Grotius Theme

## Hugo Grotius???

[Hugo Grotius](https://en.wikipedia.org/wiki/Hugo_Grotius) (Hugo de Groot) is a Dutch historical figure. 

## Social icons

The template has support for a user-defined sets of social icons.
The icons are configured through an order list 'social' in a data file called `social.yaml` in the `data` folder of your Hugo project.
The icons are sorted in the order of the file (per the ordered list).
To add a spacer between 2 icons, just create an item without a url. Just an id will do.
You can use any icon in the FontAwesome 'solid' and 'brands' styles.

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
## Credits

- [Normalize](https://necolas.github.io/normalize.css/) version 8.0.1
- [FontAwesome](https://fontawesome.com) version 5.11.2
- Wikimedia [picture of Hugo Grotius](https://commons.wikimedia.org/wiki/File:Michiel_Jansz_van_Mierevelt_-_Hugo_Grotius.jpg)