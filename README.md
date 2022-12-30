# SergioHidalgoPage

## How to configure

The theme doesn't require any advanced configuration. Just copy:

```toml
baseURL = "http://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "dimension"
```

to `config.toml` file in your Hugo root directory and change params fields.

**NOTE:** All the main page styling and configuration can be done by creating `_index.md` pages in the `content` folder and subdirectories. This choice was made to allow the use of any headless CMS (e.g. netlify) for total customization.

## Post archetype

See the basic `_index.md` file params supported by the theme — https://github.com/your-identity/hugo-theme-dimension/blob/master/archetypes/_index.md

```toml
title: Your Name
description: A great human
background: "<path or link to image>"
logo: "<path or link to image>"
```

### `background` and `logo` Params

As indicated above, `background` and `logo` can be an image of your choice by placing JPGs, PNGs, SVGs, etc. in the `static` directory of your repository. If the `static` directory does not yet exist, create it. 

Given the following repo structure:
```
  .
  ├── config.toml
  ├── content
  │   ├── posts
  │   │   └── _index.md
  │   ├── _index.md
  │   └── elements.md
  ├── static
  │   └── images
  │       ├── custom_bg.jpg  
  │       └── custom_logo.svg
  └── archetypes
      └── default.md
```

`static/images/custom_bg.jpg` can be referenced in `content/_index.md` as:
```yaml
  ---
  title: Your Name
  description: A great human
  background: "images/custom_bg.jpg"
  logo: "images/custom_logo.svg"
  ---
```

...or in `content/posts/_index.md` as:
```yaml
  ---
  title: Posts
  description: A great human's posts
  background: "../images/custom_bg.jpg"
  logo: "../images/custom_logo.svg"
  ---
```

Both fields may also be a URL to an online asset, such as:
```yaml
  ---
  title: Posts
  description: A great human's posts
  logo: "https://upload.wikimedia.org/wikipedia/commons/8/8e/Font_Awesome_5_regular_gem.svg"
  ---
```

## How to run your site

From your Hugo root directory run:

```
$ hugo serve
```

and go to `localhost:1313` in your browser. From now on all the changes you make will go live, so you don't need to refresh your browser every single time.

## Sponsoring

If you like my work and want to support the development of the project, now you can! Just:

<a href="https://www.buymeacoffee.com/luispastro" target="_blank"><img src="https://res.cloudinary.com/panr/image/upload/v1579374705/buymeacoffee_y6yvov.svg" alt="Buy Me A Coffee" ></a>


## License

Copyright © 2020 Davide Asnaghi

The theme is released under the CC BY 3.0 License. Check the [original theme license](https://github.com/your-identity/hugo-theme-dimension/blob/master/LICENSE.md) for additional licensing information.
