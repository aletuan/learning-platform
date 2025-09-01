# MCP (Model Context Protocol) Setup Documentation

## Overview
This project has been configured with MCP servers to enable AI-powered automation and design integration tools.

## Configured MCP Servers

### 1. Playwright MCP Server ✅
- **Package**: `@playwright/mcp`
- **Status**: Connected and functional
- **Purpose**: Browser automation, testing, and web scraping
- **Installation**: `npm install -g @playwright/mcp`

**Capabilities:**
- Automate web browsers (Chrome, Firefox, Safari)
- Perform UI testing
- Web scraping and data extraction
- Screenshot and PDF generation
- Form filling and interaction

### 2. Figma MCP Server ✅
- **Package**: `mcp-figma`
- **Status**: Connected and functional
- **Purpose**: Figma API integration for design workflows
- **Installation**: `npm install -g mcp-figma`

**Capabilities:**
- Access Figma files and components
- Retrieve design tokens and assets
- Export design elements
- Design system management

**Setup Requirements:**
To use Figma MCP server, you'll need a Figma Access Token:
1. Go to Figma > Account Settings > Personal Access Tokens
2. Generate a new token
3. Set the environment variable: `export FIGMA_ACCESS_TOKEN=your_token_here`

## Configuration Files

### Project-Specific Configuration (`.mcp.json`)
```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp"],
      "env": {
        "PLAYWRIGHT_BROWSERS_PATH": "0"
      }
    },
    "figma": {
      "command": "npx",
      "args": ["mcp-figma"],
      "env": {
        "FIGMA_ACCESS_TOKEN": "${FIGMA_ACCESS_TOKEN}"
      }
    }
  }
}
```

## Usage Examples

### Playwright Examples
- "Create a test that navigates to example.com and takes a screenshot"
- "Fill out the contact form on the website"
- "Check if all links on the homepage are working"

### Figma Examples
- "Export all icons from the design system"
- "Get the color palette from the main design file"
- "List all components in the Figma file"

## Management Commands

### Check MCP Server Status
```bash
claude mcp list
```

### Get Detailed Server Information
```bash
claude mcp get playwright
claude mcp get figma
```

### Remove a Server
```bash
claude mcp remove <server_name> -s local
```

### Add a New Server
```bash
claude mcp add <name> <command> [args...] -s local
```

## Troubleshooting

### Common Issues
1. **Server Connection Failed**: Check if the package is installed globally
2. **Figma Access Issues**: Ensure FIGMA_ACCESS_TOKEN is set correctly
3. **Playwright Browser Issues**: Run `npx playwright install` to install browsers

### Debugging
Use the `--mcp-debug` flag when running Claude to get detailed MCP server logs:
```bash
claude --mcp-debug
```

## Environment Variables
- `FIGMA_ACCESS_TOKEN`: Required for Figma MCP server functionality
- `PLAYWRIGHT_BROWSERS_PATH`: Set to "0" to use system browsers

## Last Updated
September 1, 2025

---
*This configuration enables powerful AI-assisted automation and design workflows through Claude's MCP integration.*
