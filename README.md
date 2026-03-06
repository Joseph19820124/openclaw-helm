# OpenClaw Custom Helm Chart

Minimal Helm chart for OpenClaw without Chromium.

## Install

```bash
helm upgrade --install openclaw-custom . --namespace default
```

## Uninstall

```bash
helm uninstall openclaw-custom
```

## Configuration

Edit `values.yaml` to customize:

- `image.tag` - OpenClaw version
- `config.gateway.controlUi.allowedOrigins` - CORS origins
- `config.browser.enabled` - Enable/disable browser (default: false)
- `skills` - List of skills to install
- `env` - Environment variables (e.g., ANTHROPIC_API_KEY)
- `resources` - CPU/memory limits

## Example: Add environment variables

```yaml
env:
  ANTHROPIC_API_KEY: "your-key-here"
  OPENAI_API_KEY: "your-key-here"
```

## Example: Add more skills

```yaml
skills:
  - weather
  - gog
  - your-skill-name
```
