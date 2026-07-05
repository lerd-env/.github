# Lerd

> Open-source, Herd-like local PHP development for Linux and macOS, with Windows
> via WSL2 (beta). Podman-native, rootless, with a built-in Web UI.

[![Docs](https://img.shields.io/badge/docs-lerd.sh-blue)](https://lerd.sh)
[![Reddit](https://img.shields.io/badge/Reddit-r%2Flerd-ff2d20?logo=reddit)](https://reddit.com/r/lerd)
[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?logo=discord&logoColor=white)](https://discord.gg/ej33c5N9s)

**lerd-env** is the home for Lerd's community and distribution repos. The main
project lives at **[lerd-env/lerd](https://github.com/lerd-env/lerd)**; the repos
here are the pieces that let Lerd grow and ship without a binary release.

`lerd link` and your project is live at `project.test` with HTTPS. No Docker, no
sudo, no system pollution. Works with Laravel, Symfony, WordPress, Drupal,
CakePHP, Statamic, and any custom PHP framework.

```bash
curl -fsSL https://lerd.sh/install.sh | bash
```

## Repositories

- **[frameworks](https://github.com/lerd-env/frameworks)**, the community
  framework store. Every `lerd link` pulls a matching definition from here, so a
  new PHP framework gains full support by editing YAML, no Lerd release required.
- **[lerd-nixos](https://github.com/lerd-env/lerd-nixos)**, the NixOS flake.
  Packages the binary and ships the `configuration.nix` blocks the stack needs
  to run Lerd declaratively.
- **[lerd-env/lerd](https://github.com/lerd-env/lerd)**, the main project: the CLI,
  the Web UI, the MCP server, and everything else.

## Why Lerd

- 🌐 Automatic `.test` domains with one-command TLS
- 🐘 Per-project PHP versions (8.1 to 8.5), switched with one click
- 🖥️ Built-in Web UI and a btop-style terminal dashboard
- 🗄️ One-click services: MySQL, PostgreSQL, Redis, Meilisearch, Mailpit, and more
- 🤖 MCP server, so AI assistants can drive your environment directly
- 🔒 Rootless and daemonless, Podman-native, no Docker required

## Get involved

Read the [docs at lerd.sh](https://lerd.sh), join the community on
[Discord](https://discord.gg/ej33c5N9s) and [r/lerd](https://reddit.com/r/lerd),
and open a pull request. Adding a framework to the
[store](https://github.com/lerd-env/frameworks) is the easiest place to start.
