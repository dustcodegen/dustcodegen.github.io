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

Current website source commit: `cae0d7e3618c37a924738447b3def9f92ab85a83`.
The source migration commit is retained in the local source worktree; this
repository deliberately does not import the archive's history or workflows.
Dust source and documentation links point to
[dustcodegen/dust](https://github.com/dustcodegen/dust). Normal installation uses
checksum-verified prebuilt binaries without Rust. The existing `v0.2.1` source
was rebuilt through [Rust-only release CI](https://github.com/dustcodegen/dust/actions/runs/38517090082);
package versions remain unchanged. Historical CLI self-upgrade behavior is
unchanged; rerun the new installer until a future release updates that destination.

Tracked deployment: [#1](https://github.com/dustcodegen/dustcodegen.github.io/issues/1).
Build dependency follow-up: [#2](https://github.com/dustcodegen/dustcodegen.github.io/issues/2).
