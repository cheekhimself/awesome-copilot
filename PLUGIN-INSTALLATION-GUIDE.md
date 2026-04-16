# Awesome Copilot Plugin Installation Guide

This guide walks you through installing and managing plugins from the Awesome Copilot marketplace.

## Prerequisites

You must have the **GitHub Copilot CLI** installed. See [installation options below](#installing-github-copilot-cli).

## Quick Start

### 1. Register the Marketplace

Register the awesome-copilot marketplace once (first-time setup):

```bash
copilot plugin marketplace add github/awesome-copilot
```

### 2. Install a Plugin

Install any available plugin from the marketplace:

```bash
copilot plugin install <plugin-name>@awesome-copilot
```

**Example:**
```bash
copilot plugin install gem-team@awesome-copilot
```

### 3. Verify Installation

List all installed plugins:

```bash
copilot plugin list
```

## Available Plugins

| Plugin Name | Description |
| --- | --- |
| `gem-team` | GEM suite: Designer, Debugger, Critic, Implementer, Reviewer, Orchestrator, Researcher, DevOps, Documentation Writer |
| `python-mcp-development` | Python MCP server development and patterns |
| `typescript-mcp-development` | TypeScript MCP server development |
| `azure-cloud-development` | Azure infrastructure, IaC, and cloud solutions |
| `copilot-sdk` | Build agentic applications with Copilot SDK |
| `project-planning` | Break Epics, create PRDs, write implementation plans |
| `testing-automation` | TDD workflows, Playwright testing, test automation |
| `csharp-dotnet-development` | C# and .NET development patterns |
| `java-development` | Java and Spring Boot development |
| `go-mcp-development` | Go MCP server development |
| `rust-mcp-development` | Rust MCP server development |
| `context-engineering` | Managing context across multi-file changes |
| `azure-cloud-development` | Azure infrastructure and cloud tools |
| `flowstudio-power-automate` | Power Automate cloud flows and RPA |
| `cast-imaging` | CAST Imaging software discovery and analysis |
| `roundup` | Personalized status briefings from Microsoft 365 |

## Installing GitHub Copilot CLI

### Windows

#### Option 1: Windows Package Manager (Recommended)

```bash
winget install GitHub.Copilot.CLI
```

#### Option 2: Download from GitHub

Download the latest release from: [github.com/github/copilot-cli](https://github.com/github/copilot-cli)

#### Option 3: GitHub CLI

```bash
gh release download --repo github/copilot-cli --pattern "*windows*"
```

### macOS

#### Option 1: Homebrew (Recommended)

```bash
brew install github/copilot-cli/copilot
```

#### Option 2: macOS GitHub Releases

[github.com/github/copilot-cli/releases](https://github.com/github/copilot-cli/releases)

### Linux

#### Option 1: Download from GitHub Releases

```bash
# Example for Linux x64
curl -LO https://github.com/github/copilot-cli/releases/download/<version>/copilot-<version>-linux-x64.tar.gz
tar xzf copilot-*.tar.gz
sudo mv copilot /usr/local/bin/
```

#### Option 2: Using snap (if available)

```bash
snap install copilot
```

## Common Commands

### Manage Marketplaces

```bash
# List registered marketplaces
copilot plugin marketplace list

# Add a marketplace
copilot plugin marketplace add github/awesome-copilot

# Remove a marketplace
copilot plugin marketplace remove github/awesome-copilot
```

### Manage Plugins

```bash
# List installed plugins
copilot plugin list

# Install a plugin
copilot plugin install <plugin-name>@awesome-copilot

# Uninstall a plugin
copilot plugin uninstall <plugin-name>

# Update a plugin
copilot plugin update <plugin-name>

# Show plugin details
copilot plugin show <plugin-name>
```

## Troubleshooting

### "Unknown marketplace" Error

If you get an error about an unknown marketplace:

```bash
# Register the marketplace first
copilot plugin marketplace add github/awesome-copilot

# Then try installing again
copilot plugin install <plugin-name>@awesome-copilot
```

### Plugin Not Found

Ensure:

1. The plugin name is spelled correctly
2. The marketplace is registered: `copilot plugin marketplace list`
3. The plugin exists in this repository: Browse [awesome-copilot.github.com/plugins](https://awesome-copilot.github.com/plugins)

### CLI Not Found

Verify the CLI is installed and in your PATH:

```bash
copilot --version
```

If not found:

- Reinstall using the [installation guide above](#installing-github-copilot-cli)
- Add the installation directory to your PATH environment variable
- Restart your terminal/shell

## Using Installed Plugins

Once installed, plugins appear as options in:

- **GitHub Copilot Chat** (VS Code)
- **GitHub Copilot CLI** commands
- **Copilot tools and workflows**

Use plugins by:

1. Opening Copilot Chat in VS Code (`Ctrl+Shift+I`)
2. Typing a request that matches the plugin's domain
3. The agent will automatically activate the relevant plugin

## More Information

- **[Awesome Copilot Website](https://awesome-copilot.github.com)**
- **[Plugin Marketplace](https://awesome-copilot.github.com/plugins)**
- **[Copilot CLI Documentation](https://github.com/github/copilot-cli)**
- [Contributing](CONTRIBUTING.md)

---

**Last Updated**: April 15, 2026
