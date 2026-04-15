# Homun Homebrew Tap

Homebrew tap for **[Homun](https://github.com/homun-app/homun)** — your personal AI assistant, single binary, privacy-first, local-first.

## Install

```bash
brew install homun-app/tap/homun
```

Or in two steps:

```bash
brew tap homun-app/tap
brew install homun
```

To get the very latest from source instead of the binary bottle:

```bash
brew install --build-from-source homun-app/tap/homun
```

After install, start the gateway:

```bash
homun gateway          # foreground
# or launch via the .app bundle on macOS
```

Open **http://localhost:8777** in your browser.

## What this tap provides

This tap only publishes the `homun` formula. It is maintained by the Homun project and released via the CI pipeline of `homun-app/homun-core` (private).

- **Source of truth**: `Formula/homun.rb` — rendered on every release from a template in the main repo
- **Binary bottle**: points to the signed+notarized `.dmg` from `homun-app/homun` releases (macOS arm64 + x64)
- **Build from source**: fallback for users who need a fresh compile

## Why a self-hosted tap and not `homebrew-core`?

`homebrew-core` requires:

- An OSI-approved open source license (Homun uses **PolyForm Noncommercial 1.0.0**, which is source-available but not OSI-approved)
- No cloud service dependencies at runtime without opt-in
- Stable tagged releases for more than 30 days

Homun is source-available (not OSI open source) by design — the source code lives in the private `homun-app/homun-core` repository and is free for personal and non-commercial use under PolyForm. That makes `homebrew-core` not an option, but a self-hosted tap has none of these requirements and is the standard path for commercial or source-available OSS projects.

## Issues and feedback

- **Formula bugs or install issues**: [homun-app/homun/issues](https://github.com/homun-app/homun/issues) (not this tap repo — please report to the main public repo for discoverability)
- **General questions**: [homun-app/homun/discussions](https://github.com/homun-app/homun/discussions)
- **Security**: [security@homun.app](mailto:security@homun.app) — see the [security policy](https://github.com/homun-app/homun/blob/main/SECURITY.md)

## License

The formula template and this README are released under **MIT** (same as the other docs in `homun-app/homun`). The actual Homun binary it installs is under **[PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0/)**.
