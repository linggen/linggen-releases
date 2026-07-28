<p align="center">
  <img src="./assets/logo.svg" alt="Linggen Logo" width="120" />
  <br />
  <a href="https://linggen.dev">https://linggen.dev</a>
</p>

## Linggen Releases

Public download host for the Linggen macOS app.

> **Linggen** is a local AI app engine — the core runtime ([engine source](https://github.com/linggen/linggen)) hosts skills as full-featured native apps. The app bundles the engine and its skills into one `.app`, served from a local daemon (`http://127.0.0.1:9527`) with all state under `~/.linggen/`.

---

## Install

```bash
curl -fsSL https://linggen.dev/install-app.sh | bash
```

Curl rather than a browser download on purpose: macOS attaches a quarantine
attribute to anything a browser fetches, and these builds are ad-hoc signed
rather than notarized, so a downloaded copy would be blocked on first launch.
The installer fetches the tarball, checks its `sha256`, and puts `Linggen.app`
in `/Applications`.

On first launch the app starts the bundled `ling` engine on `127.0.0.1:9527`,
or reuses a healthy daemon already listening there. The daemon shuts itself
down after 5 minutes idle. Updates arrive through the app's own updater.

---

## What's in it

One app, one launcher, several skills as tabs:

- **Mac Shifu** — macOS health: disk, apps, caches, plus iPhone/Mac photo and video cleanup
- **CFO** — personal finances: imports bank and credit exports, builds spend reports, learns your categories
- **DJ** — vibe to tracklist to a tagged library, synced to your phone
- **Memory** — durable cross-host memory on the `ling-mem` daemon

Mac Shifu (formerly Sys Doctor) and CFO were once separate downloads. They are
skills inside the one app now, and `linggen.dev/install-sys-doctor.sh` and
`install-cfo.sh` redirect here.

---

## Releases

| Tag pattern | Where | What |
|---|---|---|
| `linggen-v<version>` | this repo | the macOS app tarball + `.sha256` |
| `<version>`, no prefix | [`linggen/linggen`](https://github.com/linggen/linggen/releases) | the `ling` engine binary, macOS and Linux |
| `v<version>` | [`linggen/linggen-memory`](https://github.com/linggen/linggen-memory/releases) | the `ling-mem` memory daemon |

Only the app is hosted here. It bundles its own copy of the engine, so the app
version and the engine version move independently.

Builds are macOS arm64, ad-hoc signed, not notarized. The app source lives in
`linggen/linggen-app` (private); the engine, the skills, and the memory daemon
are public.
