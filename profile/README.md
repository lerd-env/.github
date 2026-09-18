# Lerd

> Local PHP development that just works. Run `lerd link` and your project is live
> at `project.test` with HTTPS. No Docker, no sudo, no system pollution.

[![Docs](https://img.shields.io/badge/docs-lerd.sh-blue)](https://lerd.sh)
[![Reddit](https://img.shields.io/badge/Reddit-r%2Flerd-ff2d20?logo=reddit)](https://reddit.com/r/lerd)
[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?logo=discord&logoColor=white)](https://discord.gg/ej33c5N9s)

Open-source, Herd-like local PHP development for Linux and macOS, with Windows via
WSL2 (beta). Nginx, PHP-FPM, and your services run as rootless Podman containers,
fronted by a built-in Web UI, a btop-style terminal dashboard, a full CLI, and an
MCP server so your AI assistant can drive the whole thing from chat.

```bash
curl -fsSL https://lerd.sh/install.sh | bash
```

Works with Laravel, Symfony, WordPress, Drupal, CakePHP, Statamic, and any custom
PHP framework.

## Why Lerd

|                    | Lerd | DDEV | Lando | Laravel Herd |
|--------------------|------|------|-------|--------------|
| Podman-native      | ✅   | 🟡   | ❌    | ❌           |
| Rootless           | ✅   | ❌   | ❌    | ✅           |
| Web UI             | ✅   | ❌   | ❌    | ✅           |
| Terminal dashboard | ✅   | ❌   | ❌    | ❌           |
| Linux              | ✅   | ✅   | ✅    | ❌           |
| macOS              | ✅   | ✅   | ✅    | ✅           |
| Windows (WSL2)     | 🧪   | ✅   | ✅    | ✅           |
| MCP server         | ✅   | ❌   | ❌    | ✅           |

## What you get

- 🌐 **Automatic `.test` domains** with one-command TLS, or opt out and use `*.localhost` with no system resolver tweak
- 🐘 **Per-project PHP** (8.1 to 8.5) switched with one click, plus a per-site FrankenPHP runtime with Laravel Octane and Symfony Runtime
- 🖥️ **Built-in Web UI** with live dashboards, a Cmd+K command palette, in-browser editing of nginx, `php.ini`, and `.env`, and fourteen languages
- 🛰️ **Debug window** that streams every `dump()` and `dd()` to the dashboard, plus SQL with N+1 and slow-query detection, mail, jobs, events, and outgoing HTTP, on Laravel and Symfony
- 🔥 **SPX profiler** — one click turns every request into a flame graph, no FPM restart and no code changes
- 🩺 **Site doctor** with framework-agnostic health checks and one-click fixes, in the UI, the TUI, the CLI, and MCP
- 📈 **Request timing** that charts response times and the slowest routes from your site's own traffic, with a click to profile the route that stands out
- 🐚 **Tinker in the browser**, a REPL against your running application, and a terminal dashboard for everything you would rather not leave the shell for
- 🗄️ **One-click services**: MySQL, PostgreSQL, Redis, Meilisearch, Mailpit, and more, each a versioned YAML preset you can update, migrate, or reset in place
- 💾 **Databases you can hand around**: export, import, and snapshots you can roll back to, next to bucket and mail management in the same dashboard
- ⚡ **Native runtime on macOS**, where PHP-FPM, the CLI and the workers run on the host instead of crossing the VM boundary for every file
- 📶 **Share a site over the LAN** with your phone or a colleague's laptop, loopback URLs in the page rewritten so the other device can follow them
- 🔔 **Desktop notifications and a system tray** for failed jobs, slow routes, captured mail and the environment's state, without a tab open
- 😴 **Idle-suspend**, which stops a quiet site's workers and brings them back on the next request, so a machine full of projects costs what you are actually using
- 🌳 **First-class git worktrees** with auto-detected branch domains, per-worktree PHP and Node versions, and optional database isolation
- 🤖 **MCP server** so Claude Code, Cursor, Copilot, and other assistants scaffold projects, run migrations, and manage services from chat
- 🔒 **Rootless and daemonless**, Podman-native, no Docker required, dual-stack IPv4 and IPv6

## Repositories

**lerd-env** is the home for Lerd's community and distribution repos.

- **[lerd](https://github.com/lerd-env/lerd)**, the main project: the CLI, the Web
  UI, the MCP server, and everything else.
- **[lerd-desktop](https://github.com/lerd-env/lerd-desktop)**, the desktop app: a
  native window around the dashboard with native desktop notifications, shipped as
  a Flatpak, pairing with Lerd running on your machine.
- **[lerd-omarchy-glance](https://github.com/lerd-env/lerd-omarchy-glance)**, the
  Omarchy bar widget: sites, services, workers and container resources in the Quattro
  bar, quiet until something breaks, so the state of the environment is on screen
  without opening a tab.
- **[frameworks](https://github.com/lerd-env/frameworks)**, the community framework
  store. Every `lerd link` pulls a matching definition from here, so a new PHP
  framework gains full support by editing YAML, no Lerd release required.
- **[services](https://github.com/lerd-env/services)**, the community service-preset
  store. Databases, caches, search engines, and admin dashboards, all as versioned
  YAML that ships without a binary release.
- **[lerd-nixos](https://github.com/lerd-env/lerd-nixos)**, the NixOS flake. Packages
  the binary and ships the `configuration.nix` blocks the stack needs to run Lerd
  declaratively.
- **[php](https://github.com/lerd-env/php)**, the static PHP builds behind the
  native runtime on macOS: an interpreter per supported version, for sites served
  straight on the host rather than in a container.
- **[homebrew-lerd](https://github.com/lerd-env/homebrew-lerd)**, the Homebrew tap,
  for `brew install lerd-env/lerd/lerd` on macOS and Linux.
- **[lerd-deb](https://github.com/lerd-env/lerd-deb)**, the Debian and Ubuntu
  packaging, published to the `ppa:lerd/lerd` Launchpad PPA.
- **[lerd-rpm](https://github.com/lerd-env/lerd-rpm)**, the Fedora packaging,
  published to COPR.

## Get involved

Read the [docs at lerd.sh](https://lerd.sh), join the community on
[Discord](https://discord.gg/ej33c5N9s) and [r/lerd](https://reddit.com/r/lerd),
and open a pull request. Adding a framework to the
[store](https://github.com/lerd-env/frameworks) is the easiest place to start.
