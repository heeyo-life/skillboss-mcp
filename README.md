# @skillboss/mcp-server

Official SkillBoss MCP Server - Access 100+ AI models and services via Model Context Protocol.

Works with **Claude Code**, **Cursor**, **Windsurf**, **OpenClaw**, and any MCP-compatible agent.

## Quick Start

### npx (Recommended)

```bash
# Run directly without installation
npx @skillboss/mcp-server
```

### Global Installation

```bash
npm install -g @skillboss/mcp-server
skillboss-mcp
```

## Configuration

### Claude Code

```bash
# Add SkillBoss MCP server
claude mcp add skillboss --command "npx" --args "-y,@skillboss/mcp-server" --env "SKILLBOSS_API_KEY=YOUR_KEY"

# Verify installation
claude mcp list
```

### Cursor / Windsurf

Add to your MCP settings (Settings > MCP Servers):

```json
{
  "skillboss": {
    "command": "npx",
    "args": ["-y", "@skillboss/mcp-server"],
    "env": {
      "SKILLBOSS_API_KEY": "YOUR_KEY"
    }
  }
}
```

### Manual Configuration

Edit `~/.mcp/servers.json`:

```json
{
  "servers": {
    "skillboss": {
      "command": "npx",
      "args": ["-y", "@skillboss/mcp-server"],
      "env": {
        "SKILLBOSS_API_KEY": "YOUR_KEY"
      }
    }
  }
}
```

## Get Your API Key

1. Visit [skillboss.co/console](https://skillboss.co/console)
2. Sign up (free tier includes 20 credits)
3. Copy your API key

## Available Tools

### `chat`
Send messages to any of 50+ AI models.

```
Available models:
- bedrock/claude-4-5-sonnet (Best for complex reasoning)
- gpt-5 (Latest OpenAI)
- gemini-2.5-flash (Fastest, 1M context)
- deepseek/deepseek-v3 (Cost-effective coding)
- and 40+ more
```

### `list_models`
List all available AI models with capabilities.

### `generate_image`
Create images using DALL-E 3 or Flux.

### `text_to_speech`
Convert text to speech with ElevenLabs or OpenAI TTS.

### `get_balance`
Check your credit balance.

### `recommend_model`
Get AI model recommendations based on your task.

## Example Usage

Once installed, your AI agent can use SkillBoss tools naturally:

```
User: "Use SkillBoss to generate an image of a sunset"

Agent: [Calls generate_image tool]
→ Image URL: https://...

User: "Ask Claude about the best Python web framework"

Agent: [Calls chat tool with model=bedrock/claude-4-5-sonnet]
→ Response: "For modern Python web development..."
```

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `SKILLBOSS_API_KEY` | Your SkillBoss API key (required) | - |
| `SKILLBOSS_BASE_URL` | API base URL | `https://api.heybossai.com/v1` |

## Pricing

SkillBoss uses pay-as-you-go pricing with **no markup** on model costs:

| Model | Input | Output |
|-------|-------|--------|
| Claude 4.5 Sonnet | $3.00/1M tokens | $15.00/1M tokens |
| GPT-5 | $15.00/1M tokens | $15.00/1M tokens |
| Gemini 2.5 Flash | $0.10/1M tokens | $0.40/1M tokens |
| DeepSeek V3 | $0.27/1M tokens | $0.27/1M tokens |

[Full pricing →](https://skillboss.co/docs/pricing/agent-pricing)

## Links

- **Documentation**: [skillboss.co/docs](https://skillboss.co/docs)
- **Console**: [skillboss.co/console](https://skillboss.co/console)
- **Discord**: [discord.gg/skillboss](https://discord.gg/skillboss)
- **GitHub**: [github.com/heeyo-life/skillboss-mcp](https://github.com/heeyo-life/skillboss-mcp)

## One-Line Install (Alternative)

If you prefer the all-in-one installer:

```bash
curl -fsSL https://skillboss.co/install.sh | bash
```

This installs the SkillBoss Skills Pack for Claude Code, Cursor, and Windsurf.

## License

MIT
