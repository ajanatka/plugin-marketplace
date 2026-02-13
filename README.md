# Plugin Marketplace

Claude Code plugin marketplace for distributing plugins.

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [compound-flow](./plugins/compound-flow/) | Python-focused compound engineering. 17 agents, 15 commands, 11 skills. | 1.2.0 |
| [design-studio](./plugins/design-studio/) | Rapid UI prototyping with design system awareness, UX best practices, and designer-level taste. 9 skills, 1 agent. | 1.0.0 |

## Installation

Plugins are installed by cloning them into your Claude Code plugins directory (`~/.claude/plugins/`). Restart Claude Code after installing.

### Install a plugin

```bash
# compound-flow
git clone https://github.com/ajanatka/compound-flow.git ~/.claude/plugins/compound-flow

# design-studio
git clone https://github.com/ajanatka/design-studio.git ~/.claude/plugins/design-studio
```

### Update a plugin

```bash
cd ~/.claude/plugins/<plugin-name> && git pull
```

## Adding a New Plugin

1. Create the plugin directory under `plugins/`:
   ```
   plugins/my-plugin/
   ├── .claude-plugin/
   │   └── plugin.json
   ├── agents/
   ├── commands/
   ├── skills/
   └── README.md
   ```

2. Add an entry to `.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "my-plugin",
     "description": "What it does.",
     "version": "1.0.0",
     "author": { "name": "Your Name" },
     "homepage": "https://github.com/...",
     "tags": ["tag1", "tag2"],
     "source": "./plugins/my-plugin"
   }
   ```

3. Update this README with the new plugin.

## Structure

```
plugin-marketplace/
├── .claude-plugin/
│   └── marketplace.json    # Marketplace catalog
├── plugins/
│   ├── compound-flow/      # Python compound engineering plugin
│   └── design-studio/      # UI prototyping and design system plugin
└── README.md
```

## License

MIT
