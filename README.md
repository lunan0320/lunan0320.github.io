# Nan Yan's website

A static academic homepage built with Jekyll and hosted on GitHub Pages.

## Local preview

With Ruby and Bundler installed:

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 4000
```

Open <http://127.0.0.1:4000>. Jekyll rebuilds the site when source files change.
Local previews do not load analytics. To generate the production site:

```sh
JEKYLL_ENV=production bundle exec jekyll build --strict_front_matter
```

The generated `_site/` directory is ignored by Git. Building or previewing does
not publish the website.

## Updating content

- `index.md`: biography, experience, and honors. Keep `last_modified_at` current
  when updating the homepage. Previously hidden material remains in a Liquid
  comment and is not included in the generated HTML.
- `_data/publications.yml`: papers, author order, and resource links. Place media
  links after PDF, Code, and other resources in the same `links` list.
  `featured: true` places a paper in Selected work; every other paper remains
  visible under More publications.
- `_data/news.yml`: news in reverse chronological order. The newest four items
  are shown initially; older entries remain available in Earlier updates. Give
  each entry an `icon` emoji for an award, paper acceptance, grant, or talk.
- `_config.yml`: profile links, navigation, description, and analytics IDs.
- `assets/css/site.css`: homepage and 404-page styling. Legacy blog templates
  retain their existing stylesheet.

Use root-relative paths for local resources, including PDFs. The existing
EmbedX filename contains a space, represented as `%20` in its link. `sitemap.xml`
automatically includes the homepage and PDFs in `file/papers/`; it contains no
CV entry.

The homepage uses `images/photo/portrait.webp` with a JPEG fallback. Both are
800 x 829 derivatives of `photo2.jpg`; the original is unchanged.
`images/social-preview.jpg` is the 1200 x 630 sharing image.

Browser and mobile bookmark icons use Northwestern University's official
[ICO](https://common.northwestern.edu/favicon.ico),
[32-pixel PNG](https://common.northwestern.edu/v8/icons/favicon-32.png), and
[180-pixel touch icon](https://common.northwestern.edu/v8/icons/favicon-180.png),
stored locally in `images/`. Their URLs include a version suffix to refresh
previously cached portrait icons.

Experience logos are stored locally in `images/logo/` and retain their original
colors and proportions. Sources:

- [Microsoft corporate logo](https://uhf.microsoft.com/images/microsoft/RE1Mu3b.png)
- [Rice University horizontal blue logo](https://www.rice.edu/sites/g/files/bxs2566/files/2019-08/Rice_University_Horizontal_Blue.svg)

The logos belong to their respective institutions and identify the listed
research experience.

News and honors use native HTML disclosure controls; publication resources,
including media links, are visible in a single wrapping row. The homepage works
without JavaScript. Analytics are loaded only in production.
