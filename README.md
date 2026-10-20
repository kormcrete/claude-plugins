# kormcrete plugins

A [Claude Code](https://code.claude.com/docs/en/plugins) plugin marketplace. It holds released versions only; each
plugin is developed in its own repository.

| Plugin | What it does | Source |
|---|---|---|
| `swing-ui-agent` | Skills and a driver sub-agent that let a coding agent drive a live Swing app and record its UI tests | [kormcrete/swing-ui-agent](https://github.com/kormcrete/swing-ui-agent) |

## Install

In Claude Code:

```text
/plugin install swing-ui-agent --marketplace kormcrete/claude-plugins
```

For a whole project, commit this to its `.claude/settings.json`; Claude Code offers the plugin to everyone who
opens the project:

```json
{
  "extraKnownMarketplaces": {
    "kormcrete": {
      "source": { "source": "github", "repo": "kormcrete/claude-plugins" }
    }
  },
  "enabledPlugins": { "swing-ui-agent@kormcrete": true }
}
```

## Updates

A new release raises the plugin's version here. `/plugin marketplace update kormcrete` fetches it; with
`"autoUpdate": true` next to `"source"` above, Claude Code does that when a session starts.

## License

Apache-2.0, see [LICENSE](LICENSE). Each plugin's files come from its own repository under the same license.
