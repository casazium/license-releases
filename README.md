# casazium/license-releases

This repository holds **no source code**. It exists only to give the
[Casazium License Server](https://docs.casazium.com/docs/license-server/intro)'s
single-executable builds a public, unauthenticated home.

## Single-executable (SEA) builds

The actual source lives in `casazium/license`, a private repository —
GitHub Release assets on a private repo aren't downloadable by anonymous
visitors, so this public mirror exists purely to work around that.

Each [Release](../../releases) mirrors a tagged build from `casazium/license`:
a `linux-x64` and a `darwin-arm64` executable, published automatically by
that repo's CI (`publish-sea.yml`) on every version tag.

Use the stable "latest" URLs — they always resolve to the newest release,
so they never need updating:

```
https://github.com/casazium/license-releases/releases/latest/download/casazium-license-linux-x64
https://github.com/casazium/license-releases/releases/latest/download/casazium-license-darwin-arm64
```

## Docker / self-hosted downloads

The Docker Compose downloads live on the docs site, not here:

- **License Server and its admin console** (recommended):
  [casazium-license-selfhosted-bundle.zip](https://docs.casazium.com/downloads/casazium-license-selfhosted-bundle.zip)
- **License Server only**:
  [casazium-license-selfhosted.zip](https://docs.casazium.com/downloads/casazium-license-selfhosted.zip)

Full installation instructions:
[docs.casazium.com](https://docs.casazium.com/docs/license-server/getting-started/installation).

## About the "Source code" links on each Release

GitHub auto-generates a `Source code (zip)`/`(tar.gz)` archive for every
tag on every public repo — there's no way to suppress them. They contain
only this README and `SECURITY.md`, not the actual product source.
