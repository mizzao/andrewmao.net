# andrewmao.net

Source for my personal website, [www.andrewmao.net](https://www.andrewmao.net) —
built with [Jekyll](https://jekyllrb.com/) and deployed to GitHub Pages.

## Requirements

See <https://jekyllrb.com/docs/installation/#requirements>.

- **Ruby 3.3.x** — matches the version GitHub Pages builds with
  (see <https://pages.github.com/versions/>). Managed locally with
  [rbenv](https://github.com/rbenv/rbenv): `rbenv install 3.3.11`.
- `bundle install` — installs the gems pinned in `Gemfile.lock`.

## Local development

```sh
bundle exec jekyll serve --watch
```

Then open <http://127.0.0.1:4000>.

## Generating a printable résumé / CV (PDF)

The `resume`, `cv`, and `cv-short` pages (tagged `class: compact`) are meant to be
saved as PDF for sharing: they widen to fill the page and drop the site footer.

Their internal links use Jekyll's `absolute_url` filter, but `jekyll serve`
rewrites the site URL to `localhost` in development — so by default those links,
and the "Andrew Mao" site title, would point at `127.0.0.1:4000`. To serve with
production URLs instead:

```sh
JEKYLL_ENV=print bundle exec jekyll serve
```

Then open <http://127.0.0.1:4000/resume/> (or `/cv/`) and use the browser's
**Save as PDF**. Links and the site title now resolve to
`https://www.andrewmao.net/...`.

Why `print`: any `JEKYLL_ENV` other than `development` keeps the `url` from
`_config.yml`. `print` is used rather than `production` so the Google Analytics
snippet — which is gated on `production` — stays off during the local print.

## Checking links

[html-proofer](https://github.com/gjtorikian/html-proofer) builds the site and
checks it for broken links and images:

```sh
bundle exec rake
```

## Updating gems

Keep the gems in step with the latest GitHub Pages release:

```sh
bundle update
```

## Deployment

[![Deploy Jekyll](https://github.com/mizzao/andrewmao.net/actions/workflows/jekyll-gh-pages.yml/badge.svg)](https://github.com/mizzao/andrewmao.net/actions/workflows/jekyll-gh-pages.yml)

Pushing to `master` triggers the GitHub Actions workflow in
[`.github/workflows/jekyll-gh-pages.yml`](.github/workflows/jekyll-gh-pages.yml),
which builds the site with GitHub Pages' preinstalled Jekyll and publishes it to
GitHub Pages.
