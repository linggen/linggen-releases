<p align="center">
  <img src="./assets/logo.svg" alt="Linggen Logo" width="120" />
  <br />
  <a href="https://linggen.dev">https://linggen.dev</a>
</p>

## Linggen Releases

Public download host for branded Linggen apps on macOS. All published builds are codesigned and notarized.

> **Linggen** is a local AI app engine — the core runtime ([engine source](https://github.com/linggen/linggen)) hosts skills as full-featured native apps. Each branded app bundles the engine + a primary skill into one `.app`. Apps share a local daemon (`http://127.0.0.1:9898`) and the `~/.linggen/` data directory.

---

## Apps

### Sys Doctor — *coming soon*

On-device macOS health analyst. Inspects disk, memory, processes, network, security, and battery; explains findings in plain English; suggests cleanup with copy-paste commands.

- Tag scheme (when released): `sys-doctor-v<version>`
- Source: [linggen/linggen-app](https://github.com/linggen/linggen-app) (private)

*More branded apps planned (House Keeper, Majiang, Suanming, …) — see the roadmap.*

---

## Install (once a DMG is published)

1. Download the `.dmg` for the app you want from [Releases](https://github.com/linggen/linggen-releases/releases).
2. Open it; drag the app into `/Applications`.
3. First launch: the app spawns the bundled `ling` engine on `127.0.0.1:9898` (or reuses one already running). The daemon self-terminates after 5 min idle.

All Linggen apps share one local daemon and one `~/.linggen/` directory (sessions, memory, skills, credentials).

---

## Tag schemes

| Tag pattern | Where | What |
|---|---|---|
| `<app>-v<version>` | this repo | branded native app `.dmg` (e.g. `sys-doctor-v0.1.0`) |
| `v<version>` | [`linggen/linggen`](https://github.com/linggen/linggen/releases) | the `ling` CLI / engine binary on its own |

The engine binary is **not** published here. Branded apps bundle their own copy of `ling`; this repo only hosts the user-facing app DMGs.
