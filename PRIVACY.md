# CAIIDE++ Privacy Statement

## Our Commitment to Privacy

CAIIDE++ is built with privacy as a core principle. Unlike the upstream VS Code, CAIIDE++ has had all telemetry completely removed.

## Data Collection

**CAIIDE++ collects no data.** Period.

We do not:
- Collect crash reports
- Track usage analytics
- Monitor extension installations
- Record any user behavior
- Send any data to Microsoft, Anthropic, or any third party
- Phone home in any way

## What Was Removed

The following telemetry systems from VS Code have been completely stripped:

1. **Application Insights** - Microsoft's telemetry service
2. **1DS (One Data Strategy)** - Microsoft's data collection framework
3. **Experiment Framework** - A/B testing and feature flagging
4. **Crash Reporter** - Automatic crash report submission
5. **Extension Telemetry** - Extension usage tracking
6. **Settings Sync Telemetry** - Settings synchronization analytics

## Local Data Storage

CAIIDE++ stores data only on your local machine:

- **Settings**: `~/.caiide/` (user settings, keybindings)
- **Extensions**: `~/.caiide/extensions/` (installed extensions)
- **Memory MCP**: Wherever you configure (default: `~/.claude-code-pp/memory/`)

## Third-Party Services

### Open VSX Marketplace

CAIIDE++ uses [Open VSX](https://open-vsx.org) for extensions. When you:
- Browse extensions: Your IP may be logged by Open VSX servers
- Install extensions: Download requests are made to Open VSX CDN

Open VSX is operated by the Eclipse Foundation. See their [privacy policy](https://www.eclipse.org/legal/privacy.php).

### Memory MCP (Optional)

If you use the built-in Memory MCP extension:
- All data stays local by default
- Memory is stored in SQLite/Redis on your machine
- No cloud synchronization unless you explicitly configure it

## Network Requests

CAIIDE++ makes network requests only when you explicitly:
- Install/update extensions from Open VSX
- Use features that require network (e.g., GitHub integration)
- Use Memory MCP with external services (if configured)

## Verification

You can verify our privacy claims:
1. Run CAIIDE++ with network monitoring (e.g., Little Snitch, Wireshark)
2. Inspect the source code - telemetry modules are stubbed out
3. Check the product.json - `enableTelemetry: false`

## Questions?

If you have privacy concerns, open an issue at:
https://github.com/halfservers/caiide/issues
