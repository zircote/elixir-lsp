# elixir-lsp

[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Claude Plugin](https://img.shields.io/badge/claude-plugin-orange.svg)](https://docs.anthropic.com/en/docs/claude-code/plugins)
[![Marketplace](https://img.shields.io/badge/marketplace-zircote--lsp-purple.svg)](https://github.com/zircote/lsp-marketplace)
[![Elixir](https://img.shields.io/badge/Elixir-4B275F?logo=elixir&logoColor=white)](https://elixir-lang.org/)

A Claude Code plugin providing comprehensive Elixir development support through:

- **ElixirLS** integration for IDE-like features
- **Automated hooks** for formatting, linting, and testing
- **Elixir ecosystem** integration (Mix, Credo, Dialyzer)

## Quick Setup

```bash
# Run the setup command (after installing the plugin)
/setup
```

Or manually:

```bash
# Install ElixirLS (download from GitHub releases)
# https://github.com/elixir-lsp/elixir-ls/releases

# Install development tools (via Mix)
mix local.hex --force
mix local.rebar --force
mix archive.install hex credo --force
```

## Features

### LSP Integration

The plugin configures ElixirLS for Claude Code via `.lsp.json`.

**Capabilities:**
- Go to definition / references
- Hover documentation
- Code completion
- Dialyzer integration
- Real-time diagnostics

### Automated Hooks

| Hook | Trigger | Description |
|------|---------|-------------|
| `mix-format` | `**/*.ex` | Code formatting |
| `credo` | `**/*.ex` | Linting |
| `elixir-todo-fixme` | `**/*.ex` | Surface TODO/FIXME comments |

## Required Tools

| Tool | Installation | Purpose |
|------|--------------|---------|
| `elixir-ls` | GitHub releases | LSP server |
| `mix format` | Built-in | Formatting |
| `credo` | `mix archive.install hex credo` | Linting |

## License

MIT
