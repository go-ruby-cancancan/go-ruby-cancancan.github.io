<p align="center"><img src="https://raw.githubusercontent.com/go-ruby-cancancan/brand/main/social/go-ruby-cancancan.png" alt="go-ruby-cancancan/go-ruby-cancancan.github.io" width="720"></p>

# go-ruby-cancancan.github.io

The organization's institutional landing page, served at
<https://go-ruby-cancancan.github.io> and built with [Hugo](https://gohugo.io). It is a
single page (custom `layouts/index.html`).

Documentation lives in a separate repository,
[go-ruby-cancancan/docs](https://github.com/go-ruby-cancancan/docs), served at
<https://go-ruby-cancancan.github.io/docs/>. This page links there.

`.github/workflows/deploy-pages.yml` builds the landing with Hugo and deploys it
to GitHub Pages on every push to `main`.

## Local preview

```bash
hugo server      # http://localhost:1313
```

## The design is not here

It comes from the shared Hugo module
[`go-fleettools/landingkit`](https://github.com/go-fleettools/landingkit),
pinned in `go.mod` (Renovate bumps it); `kit.go` keeps `go mod tidy` from
deleting that requirement. `[params.brand]` in `hugo.toml` is read from the logo by
`landingkit brand`. A file under `layouts/partials/` with the name of one of the
kit's would silently override it.
