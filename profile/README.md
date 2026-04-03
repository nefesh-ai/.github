# Nefesh AI

**The first nervous system for AI.**

Nefesh is a B2B middleware API that translates live biometric signals into adaptive AI behavior. One endpoint, any sensor, any device.

### What we build

| Repository | Description |
|---|---|
| [nefesh-mcp-server](https://github.com/nefesh-ai/nefesh-mcp-server) | MCP + A2A server for AI agents (6 MCP tools, 4 A2A skills) |
| [nefesh-cli](https://github.com/nefesh-ai/nefesh-cli) | Official CLI: `npm install -g @nefesh/cli` |
| [nefesh-sdk](https://github.com/nefesh-ai/nefesh-sdk) | Official TypeScript SDK |
| [human-state-protocol](https://github.com/nefesh-ai/human-state-protocol) | Open specification for human state exchange between AI systems |
| [nefesh-examples](https://github.com/nefesh-ai/nefesh-examples) | Integration examples (Python, JavaScript, curl) |
| [nefesh-a2a](https://github.com/nefesh-ai/nefesh-a2a) | A2A v1.0 agent reference implementation |
| [nefesh-wearables](https://github.com/nefesh-ai/nefesh-wearables) | Wearable integration (Polar H10, Garmin, Pixel Watch) |

### Quick start

```bash
curl -X POST https://api.nefesh.ai/v1/ingest \
  -H "X-Nefesh-Key: YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"session_id":"demo","heart_rate":72,"timestamp":"2026-01-01T00:00:00Z"}'
```

Free tier: 1,000 API calls/month, no credit card.

[Get API Key](https://nefesh.ai/signup) | [Documentation](https://nefesh.ai/docs) | [Live Demo](https://sandbox.nefesh.ai) | [Website](https://nefesh.ai)
