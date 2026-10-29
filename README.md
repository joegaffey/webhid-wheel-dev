# WebHID Wheel Dev

Development preview of [webhid-wheel](https://github.com/joegaffey/webhid-wheel),
served at <https://joegaffey.com/webhid-wheel-dev/>.

This repository does not contain a copy of the source. The Pages workflow checks
out a selected branch or tag from `joegaffey/webhid-wheel`, assembles the demo
site, and deploys it. The stable site at
<https://joegaffey.com/webhid-wheel/> is deployed separately and is not affected
by this repository.

## Deploy

```sh
gh workflow run pages.yml -R joegaffey/webhid-wheel-dev \
  -f ref=main
```

The `ref` input accepts any branch or tag in `joegaffey/webhid-wheel`.

The demo imports the package source directly, so no build step is required. The
workflow publishes only the demo files (`index.html`, `script.js`, `src/` and
`.nojekyll`).
