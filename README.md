# MCP Project Finder

A fast project discovery and navigation tool for managing your code projects.

## Features

- **list_projects** - List all projects with optional filtering
- **find_project** - Fuzzy search for projects by name  
- **project_info** - Get detailed info about a project (type, files, git status)
- **recent_projects** - List recently modified projects

## Configuration

The tool uses the `CODE_PATH` environment variable to determine where to look for projects. If not set, it defaults to the parent directory of where this tool is installed.

**Environment Variables:**
- `CODE_PATH` (optional): Path to your code directory. Defaults to parent directory of this project.

## Installation

```bash
cd /path/to/mcp-project-finder
npm install
```

## Add to Claude Desktop

Add this to your Claude Desktop configuration:

```json
{
  "mcpServers": {
    "project-finder": {
      "command": "node",
      "args": ["/path/to/mcp-project-finder/server.js"],
      "env": {
        "CODE_PATH": "/your/code/directory"
      }
    }
  }
}
```

**Example configurations:**

```json
// Use default (parent directory)
{
  "project-finder": {
    "command": "node",
    "args": ["/Users/bard/Code/mcp-project-finder/server.js"],
    "env": {}
  }
}

// Custom code path
{
  "project-finder": {
    "command": "node",
    "args": ["/Users/bard/Code/mcp-project-finder/server.js"],
    "env": {
      "CODE_PATH": "/Users/bard/Projects"
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

The tool is optimized for speed - it directly lists the configured code directory instead of searching the entire filesystem.

## Default Behavior

When no `CODE_PATH` is specified, the tool automatically uses the parent directory of where it's installed. For example:
- Tool installed at: `/Users/bard/Code/mcp-project-finder/`
- Default search path: `/Users/bard/Code/`

This makes it easy to set up without any configuration while still being flexible for different environments.
