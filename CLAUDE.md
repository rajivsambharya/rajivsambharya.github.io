# rajivsambharya.github.io

Personal academic site: Jekyll 3 (`github-pages` gem) with the Minimal Mistakes theme, deployed by GitHub Pages from `master`.

## Running locally

Run this from the repo root. It serves at http://localhost:4000 and live-reloads when a file is saved:

```
LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8 PATH=/opt/homebrew/opt/ruby@3.2/bin:$PATH bundle exec jekyll serve --config _config.yml,_config.dev.yml
```

The first build takes about 10–20 seconds. Run the command in the background and poll `curl -s -o /dev/null -w "%{http_code}" http://localhost:4000/` until it returns 200.

Why each part matters:
- **Ruby 3.2, not the default Ruby.** `/opt/homebrew/bin/ruby` is Ruby 4.x, and Jekyll 3 fails there (`cannot load such file -- csv`). The Homebrew `ruby@3.2` keg already has all the gems installed.
- **UTF-8 locale.** Without it, the Sass build fails with `Invalid US-ASCII character "\xE2"` in `assets/css/style.scss`.
- **`_config.dev.yml`** sets `url` to localhost and turns off analytics.

If gems are missing (for example after a Ruby update), run `PATH=/opt/homebrew/opt/ruby@3.2/bin:$PATH bundle install`. Never run `bundle install` with the default Ruby 4: it rewrites `Gemfile.lock` with downgraded versions. If that happens, revert it with `git checkout Gemfile.lock`.

You can ignore these warnings: "No GitHub API authentication" and "install `faraday-retry`".

## Layout

- `_pages/about.md` is the home page, including news.
- `_pages/publications.md` holds the publications. Each entry is a hand-written `<div class="pub-entry">` with buttons and CSS defined inline at the top of the file. The award badge style is `.award-badge`.
- `files/CV.pdf` is the CV, and `slides/` holds talk slides.
- `_site/` is build output and is gitignored.
