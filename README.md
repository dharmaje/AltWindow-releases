# AltWindow — Downloads

Public downloads for **AltWindow**, a native macOS **companion app** for Claude Code. The Claude Code client stays exactly as it is — run it in whatever terminal you like — and AltWindow renders **live companion windows** from Claude Code's hook events.

🌐 **[altwindow.com](https://altwindow.com)** · This repo hosts the public installers only; the app source is private.

## Download

- **Latest build** (rolling, auto-updated on every change) — direct download, no login:
  **[AltWindow-latest.dmg](https://github.com/dharmaje/AltWindow-releases/releases/download/latest/AltWindow-latest.dmg)**
- **All builds** — the [Releases](https://github.com/dharmaje/AltWindow-releases/releases) page lists the rolling `latest` prerelease plus stable, versioned (`vX.Y.Z`) releases.

> The `latest` build always tracks the newest code and may be rough. For a stable build, pick a versioned release.

## Install

1. Open the downloaded `.dmg`.
2. Drag **AltWindow** to **Applications**.
3. Launch it — it offers to install the Claude Code hooks on first run.

**Requirements:** macOS 15+, Apple silicon, and [`jq`](https://jqlang.github.io/jq/).

**Gatekeeper:** the bundle is ad-hoc signed (no Apple Developer ID), so on first launch **right-click → Open** to allow it.

## Reporting bugs

Found a problem or have an idea? Please file it on the [Issues](https://github.com/dharmaje/AltWindow-releases/issues) page:

- 🐞 **[Report a bug](https://github.com/dharmaje/AltWindow-releases/issues/new?template=bug_report.yml)** — the form asks for your macOS version, AltWindow build, and repro steps.
- 💡 **[Request a feature](https://github.com/dharmaje/AltWindow-releases/issues/new?template=feature_request.yml)**

Before reporting, grab the newest [release](https://github.com/dharmaje/AltWindow-releases/releases) — your issue may already be fixed.

## License

The app is free to download and use; redistribution is permitted only as the unmodified installer. See [LICENSE](LICENSE). The app source is closed.

---

AltWindow is an independent project created by Jason Epel — not affiliated with, endorsed by, or sponsored by Anthropic. "Claude" and "Claude Code" are trademarks of Anthropic, PBC.

© 2026 Jason Epel
