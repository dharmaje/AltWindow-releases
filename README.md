# AltWindow — Downloads

Public downloads for **AltWindow**, a native macOS **companion app** for Claude Code. The Claude Code client stays exactly as it is — run it in whatever terminal you like — and AltWindow renders **live companion windows** from Claude Code's hook events.

🌐 **[altwindow.com](https://altwindow.com)** · This repo hosts the public installers only; the app source is private.

## What it does

AltWindow renders live, independently managed macOS windows from Claude Code's hook events:

- **Activity** — one row per tool call (running / done / failed) with expandable detail and colored diffs, grouped by subagent. It follows the tail as work streams in; scroll up to read back and a button resumes auto-scroll.
- **Tasks** — a live, white-on-black checklist that **opens itself when tasks appear** and **highlights what just changed** (then fades), with checkbox status icons.
- **Per-session windows** — split any session into its own Activity + Tasks pair to lay several sessions out side-by-side or stacked, then combine them back from any window. Jump straight to a window's paired Activity/Tasks window. Always-on-top and transparency are **per window**.

Your Claude Code client is never touched — no embedding, no patching; the companion only reads hook events.

## Download

- **Latest build** (rolling, auto-updated on every change) — direct download, no login:
  **[AltWindow-latest.dmg](https://github.com/dharmaje/AltWindow-releases/releases/download/latest/AltWindow-latest.dmg)**
- **All builds** — the [Releases](https://github.com/dharmaje/AltWindow-releases/releases) page lists the rolling `latest` prerelease plus stable, versioned (`vX.Y.Z`) releases.

> The `latest` build always tracks the newest code and may be rough. For a stable build, pick a versioned release.

## Install

**Easiest — paste one line into Terminal:**

```sh
curl -fsSL https://github.com/dharmaje/AltWindow-releases/releases/download/latest/install.sh | sh
```

It downloads the latest build, copies AltWindow to **Applications**, and launches it with **no Gatekeeper dialog**. On launch it offers to install the Claude Code hooks — accept to finish.

**Requirements:** macOS 15+ and Apple silicon. ([`jq`](https://jqlang.github.io/jq/) is used by the hook installer and downloaded automatically — pinned and checksum-verified — if you don't already have it.)

**Why Terminal?** AltWindow is ad-hoc signed, not notarized. On macOS 15 (Sequoia), anything a *browser* downloads — an app or an installer — is quarantined and hits a dead-end "Apple could not verify… is free of malware" dialog with no **Open** button. A `curl`-fetched install isn't quarantined, so it sidesteps that entirely.

**Prefer the DMG?** [Download it](https://github.com/dharmaje/AltWindow-releases/releases/download/latest/AltWindow-latest.dmg), drag **AltWindow** to **Applications**, then clear the quarantine so it opens: `xattr -dr com.apple.quarantine /Applications/AltWindow.app` (or System Settings → Privacy & Security → **Open Anyway**). On Sequoia the old right-click → Open no longer bypasses Gatekeeper for un-notarized apps.

## Uninstall

Removes the Claude Code hooks (backing up your settings first), deletes AltWindow from **Applications**, and clears the event spool — one line:

```sh
curl -fsSL https://github.com/dharmaje/AltWindow-releases/releases/download/latest/uninstall.sh | sh
```

## Feedback

Bug reports and feature ideas are both very welcome — pick the right form and we'll take it from there:

- 🐞 **[Report a bug](https://github.com/dharmaje/AltWindow-releases/issues/new?template=bug_report.yml)** — the form asks for your macOS version, AltWindow build, and repro steps. Before reporting, grab the newest [release](https://github.com/dharmaje/AltWindow-releases/releases) in case it's already fixed.
- 💡 **[Request a feature](https://github.com/dharmaje/AltWindow-releases/issues/new?template=feature_request.yml)** — tell us the problem you'd like AltWindow to solve.

See the [reporting guide](https://github.com/dharmaje/AltWindow-releases/wiki/Reporting-Bugs) for tips on writing a useful report.

## License

The app is free to download and use; redistribution is permitted only as the unmodified installer. See [LICENSE](LICENSE). The app source is closed.

---

AltWindow is an independent project created by Jason Epel — not affiliated with, endorsed by, or sponsored by Anthropic. "Claude" and "Claude Code" are trademarks of Anthropic, PBC.

© 2026 Jason Epel
