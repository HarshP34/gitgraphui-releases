# Git Graph UI

A free desktop Git client for Windows — visual commit graph, split diff viewer, conflict resolver, staging, branching, and remote operations. Everything runs **locally** on your machine; your repos never leave your PC.

> This repository contains **release downloads only** (installers and update metadata). Source code is not published here.

---

## Download

**Latest version (recommended):**

[![Download](https://img.shields.io/github/v/release/HarshP34/gitgraphui-releases?label=Download&style=for-the-badge)](https://github.com/HarshP34/gitgraphui-releases/releases/latest)

### System requirements

- Windows 10 or later (64-bit)
- [Git for Windows](https://git-scm.com/download/win) installed (for SSH and git commands)

### Install

1. Download the `.exe` from [Releases](https://github.com/HarshP34/gitgraphui-releases/releases/latest).
2. Run the installer and follow the prompts.
3. Open **Git Graph UI** from the Start menu or desktop shortcut.
4. Click **Open Folder** and choose a folder that contains a `.git` directory.

The app checks this repo for updates automatically when a newer version is published.

---

## Screenshots

### Git graph
![Git commit graph](./images/graph.png)



---

## Features

### Git Graph
Visual commit tree with branch lanes, colors, and auto-refresh via WebSocket whenever git state changes. Branch labels show real remote sync status (ahead, behind, or in sync). Connector lines stay clean when a commit’s parent sits in another column. Right-click any commit to cherry-pick, revert, create a branch, or copy its hash.

### Staging Area
Stage, unstage, or discard individual files, with a discard-all option for unstaged changes and confirmation prompts when needed.

### Split Diff Viewer
Side-by-side before/after diff with syntax highlighting, hunk navigation, intra-line change highlighting, and options to view changed hunks or the full file.

### Minimap Sidebar *(full file view)*
A two-column minimap alongside the diff — left half for removed lines (red), right half for added lines (green). Click any mark to scroll directly to that change. Positions are computed from rendered row index (including blank alignment rows), so clicks always land at the right spot.

### Conflict Resolver
Side-by-side Ours vs. Theirs view with per-conflict Accept/Reject controls. The panel shows whether conflicts are from a branch merge or from putting your parked local changes back. After a pull, the app checks the repository itself — not just git’s exit code — so conflict markers are never missed.

### Branch Management
Checkout, create, delete, merge, and rebase branches from the UI. Merge and rebase work even with uncommitted changes — your work is parked automatically and restored when the operation finishes. **Reset** uses a compact dialog with clear options.

### Drag-and-Drop Merge
Drag any branch badge in the graph and drop it onto the HEAD badge to open a merge popup with options for standard merge, merge without fast-forward, rebase onto source, or fast-forward only.

### Remote Operations
Fetch, pull, push, and stash (push/pop) from the toolbar.

**Pull with local changes** — pull, merge, and rebase run without committing or stashing first. Uncommitted work is parked in the stash and restored when done. If incoming files clash with new local files, your copies are saved aside and you are told where to find them.

**Push rejected** — when a push fails, choose pull & rebase then push, pull (merge) then push, force-with-lease, or hard force. Each option explains what it will do; both force options require confirmation.

**Stash reminders** — if parked work is still sitting in the stash, a notice lets you keep or discard it. Your choice is remembered per repository. Dropping one entry while another is queued is handled cleanly.


| Theme | Style |
|---|---|
| **Dark Black** | Pure black, neutral grey — no colour tint |
| **Tokyo Night** | Dark navy/blue |
| **Dracula** | Dark purple/violet |
| **One Dark** | Atom/VSCode cool grey |
| **GitHub Dark** | GitHub's official dark mode |
| **Catppuccin Mocha** | Soft pastel dark |
| **Solarized Dark** | Classic teal-tinted dark |
| **Monokai** | Warm dark with vibrant greens |

All UI elements — including diff alignment stripes — adapt to the active theme.

Zoom range: 30%–300%.

---

## Updates

New versions are published on the [Releases](https://github.com/HarshP34/gitgraphui-releases/releases) page. Installed apps notify you when an update is available and can download and install it from this repository.

To see what changed, open the release notes on each version tag.

---

## Privacy

Git Graph UI runs a small local server on your machine to talk to Git. It does not upload your repository contents to the cloud. Network access is used only for optional features you enable (e.g. `git push` / `git pull` to your remotes).

---

<p align="center">
  <sub>Release artifacts only · Built with Electron</sub>
</p>
