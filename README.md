# casazium/license-releases

This repository holds **no source code**. It exists only to give
downloadable artifacts for the
[Casazium License Server](https://docs.casazium.com/docs/license-server/)
a public, unauthenticated home — for two different reasons, so it hosts
two different kinds of artifact:

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

## Self-hosted quickstart package

`casazium-license-selfhosted.zip` — a `docker-compose.yml`, `.env.example`,
and a short README, wired up to get a self-hosted deployment running
quickly. Unlike the SEA builds above, this one is a plain tracked file
in this repo (small enough that git doesn't mind, and there's no CI
producing it).

**This copy is a backup mirror, not the live link.** The zip never had
the two problems that forced the SEA builds to live here (it's tiny,
and its source was never private), so `docs.casazium.com` links its own
same-origin copy (`docs/public/downloads/casazium-license-selfhosted.zip`
in `casazium/casazium`) directly — a same-domain download is better UX
than sending visitors to a raw `github.com` URL for no real benefit.
When the zip's contents change, update both copies by hand; only the
SEA builds are the authoritative, single-source artifact here.

Full installation instructions:
[docs.casazium.com](https://docs.casazium.com/docs/license-server/getting-started/installation).

## About the "Source code" links on each Release

GitHub auto-generates a `Source code (zip)`/`(tar.gz)` archive for every
tag on every public repo — there's no way to suppress them. They contain
only this README, not the actual product source.
