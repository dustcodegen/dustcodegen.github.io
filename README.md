# dust

The existing dust website and field-note blog, published at
[dustcodegen.github.io](https://dustcodegen.github.io/).

This repository contains compiled static output only. GitHub Pages serves
`main` from the repository root. Keep `.nojekyll` to preserve `_astro/` assets.
No custom CI, social-publishing workflow, credentials or Node server is deployed.

## Updating the site

Build from the existing `dust-linkedin` source archive:

```sh
npm ci
npm test
npm run build
npm run check:pages
```

Copy the validated `dist/` contents (including `.nojekyll`) into a clean
deployment branch, review the diff and merge its pull request. Remove obsolete
generated assets when replacing a later build, not repository metadata.

Initial source commit: `e9abd7bd1cd928f561d883f4fd227e3afed6044a`.
The source migration commit is retained in the local source worktree; this
repository deliberately does not import the archive's history or workflows.
The original Dust documentation and installation links remain unchanged.

Tracked deployment: [#1](https://github.com/dustcodegen/dustcodegen.github.io/issues/1).
Build dependency follow-up: [#2](https://github.com/dustcodegen/dustcodegen.github.io/issues/2).
