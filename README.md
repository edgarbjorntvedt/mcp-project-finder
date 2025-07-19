# MCP Project Finder

A fast project discovery and navigation tool for `/Users/bard/Code`.

## Features

- **list_projects** - List all projects with optional filtering
- **find_project** - Fuzzy search for projects by name  
- **project_info** - Get detailed info about a project (type, files, git status)
- **recent_projects** - List recently modified projects

## Installation

```bash
cd /Users/bard/Code/mcp-project-finder
npm install
```

## Add to Claude Desktop

Add this to your Claude Desktop configuration:

```json
{
  "mcpServers": {
    "project-finder": {
      "command": "node",
      "args": ["/Users/bard/Code/mcp-project-finder/server.js"],
      "env": {}
    }
  }
}
```

## Usage Examples

Once installed, you can use these commands:

- "List all my projects"
- "Find the brain project"  
- "Show me recent projects"
- "Get info about mcp-brain-manager"

The tool is optimized for speed - it directly lists the Code directory instead of searching the entire filesystem.
