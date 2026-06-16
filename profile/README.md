# cc-mods

A small, modular suite for playing **[CrossCode](https://store.steampowered.com/app/368340/CrossCode/)**
your way — on **desktop** and on **iPhone/iPad** — built around the
[CCLoader](https://github.com/CCDirectLink/CCLoader) modding ecosystem.

> ⚠️ You must own CrossCode. Nothing here contains the game's code or assets — only wrappers, mods,
> and tooling. Unofficial fan projects, **not affiliated with Radical Fish Games**.

## The suite

| Repo | What it is | Desktop | iOS (cc-ios) |
|---|---|:---:|:---:|
| **[cc-ios](https://github.com/cc-mods/cc-ios)** | Native WKWebView wrapper that runs CrossCode on iPhone/iPad (the iOS analog of CrossAndroid) | — | ✅ platform |
| **[cc-ultrawide](https://github.com/cc-mods/cc-ultrawide)** | True ultrawide (21:9) field of view with pixel-perfect integer scaling | ✅ | ✅ |
| **[cc-aimassist](https://github.com/cc-mods/cc-aimassist)** | Gentle controller aim assist (locks onto a nearby enemy; spread untouched) | ✅ | ✅ |
| **[cc-iostitlebuttons](https://github.com/cc-mods/cc-iostitlebuttons)** | Native Restart/Close title-screen buttons for cc-ios (no-op on desktop) | ⏸️ disabled | ✅ |
| **[cc-tailsync](https://github.com/cc-mods/cc-tailsync)** | Wireless save sync over Tailscale (iOS library + macOS/Windows save-servers) | ✅ server | ✅ |
| **[CCModDB](https://github.com/cc-mods/CCModDB)** | The mod database CCModManager reads for one-click installs | ✅ | ✅ |

## Design principles

- **Absolute compatibility, full modularity.** Install just **cc-ios** for your phone, or any mod on
  desktop on its own, or all of them together. Nothing hard-depends on another mod.
- **One-click everywhere.** Each mod ships a `.ccmod` GitHub Release and is listed in
  **[CCModDB](https://github.com/cc-mods/CCModDB)**, so it installs (and auto-updates) from the
  in-game **Mods** tab. cc-ios pre-registers the database, so the suite is one-click on the phone
  out of the box.
- **cc-ios-safe by construction.** Every mod follows the wrapper's browser-mode rules (no undeclared
  assets, no unguarded desktop-only APIs), so the same `.ccmod` runs on desktop **and** iOS.
- **No game assets, ever.** You bring your own legally-owned copy; these repos ship none.

## Quick start

- **On iPhone:** set up **[cc-ios](https://github.com/cc-mods/cc-ios)** (`make tui`), then install
  mods one-click from the in-game **Mods** tab.
- **On desktop:** install [CCLoader](https://github.com/CCDirectLink/CCLoader) +
  [CCModManager](https://github.com/CCDirectLink/CCModManager), add the `@cc-mods/CCModDB/stable`
  repository in its settings, and install from the **Online** tab — or just drop a `.ccmod` from any
  repo's Releases into `CrossCode/assets/mods/`.
- **Sync saves between them:** **[cc-tailsync](https://github.com/cc-mods/cc-tailsync)**.

## Credits

Built on the work of the CrossCode modding community —
[CCLoader](https://github.com/CCDirectLink/CCLoader),
[CCModManager](https://github.com/CCDirectLink/CCModManager), and
[CCModDB](https://github.com/CCDirectLink/CCModDB) by **CCDirectLink**, and
[CrossAndroid](https://gitlab.com/Namnodorel/crossandroid) by **Namnodorel**. CrossCode by
**Radical Fish Games**.
