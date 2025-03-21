# Framer Plugin MCP Server

[![smithery badge](https://smithery.ai/badge/@Sheshiyer/framer-plugin-mcp)](https://smithery.ai/server/@Sheshiyer/framer-plugin-mcp)

A Model Context Protocol (MCP) server that enables creation and management of Framer plugins with web3 capabilities. This server provides tools for creating, building, and managing Framer plugins with integrated web3 features like wallet connections, contract interactions, and NFT displays.

## Features

- Create new Framer plugins with web3 capabilities
- Build plugins for production
- Integrated web3 features:
  - Wallet Connect integration
  - Smart contract interactions
  - NFT display components

## Requirements

- Node.js 16 or higher
- NPM or Yarn
- Framer desktop app for testing plugins

## Installation

### Installing via Smithery

To install Framer Plugin Server for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@Sheshiyer/framer-plugin-mcp):

```bash
npx -y @smithery/cli install @Sheshiyer/framer-plugin-mcp --client claude
```

### Manual Installation
1. Clone this repository:
```bash
git clone https://github.com/sheshiyer/framer-plugin-mcp.git
cd framer-plugin-mcp
```

2. Install dependencies:
```bash
npm install
```

3. Build the server:
```bash
npm run build
```

## Configuration

Add the server to your MCP settings file:

For Claude Desktop App (`~/Library/Application Support/Claude/claude_desktop_config.json`):
```json
{
  "mcpServers": {
    "framer-plugin": {
      "command": "node",
      "args": ["/path/to/framer-plugin-mcp/build/index.js"]
    }
  }
}
```

For Cursor/Claude Dev (`~/Library/Application Support/Cursor/User/globalStorage/saoudrizwan.claude-dev/settings/cline_mcp_settings.json`):
```json
{
  "mcpServers": {
    "framer-plugin": {
      "command": "node",
      "args": ["/path/to/framer-plugin-mcp/build/index.js"]
    }
  }
}
```

## Usage

Once configured, the server provides the following tools:

### create_plugin
Creates a new Framer plugin project with web3 capabilities.

Parameters:
- name: Plugin name
- description: Plugin description
- outputPath: Output directory path
- web3Features: Array of features to include (wallet-connect, contract-interaction, nft-display)

Example:
```json
{
  "name": "my-web3-plugin",
  "description": "A Framer plugin with web3 features",
  "outputPath": "./plugins/my-web3-plugin",
  "web3Features": ["wallet-connect", "nft-display"]
}
```

### build_plugin
Builds a Framer plugin project for production.

Parameters:
- pluginPath: Path to plugin directory

Example:
```json
{
  "pluginPath": "./plugins/my-web3-plugin"
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details
