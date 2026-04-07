# Nefesh AI

**The first nervous system for AI.**

Nefesh is a B2B middleware API that translates live biometric signals into adaptive AI behavior in real time. Any sensor, any device, any LLM. One HTTP POST, no SDK required.

Listed on the official MCP registries: [Smithery](https://smithery.ai), [Glama](https://glama.ai), [PulseMCP](https://pulsemcp.com).

### What we build

| Repository | Description |
|---|---|
| [nefesh-mcp-server](https://github.com/nefesh-ai/nefesh-mcp-server) | MCP + A2A server for AI agents (6 MCP tools, 4 A2A skills) |
| [nefesh-gateway](https://github.com/nefesh-ai/nefesh-gateway) | Cognitive Compute Router: 3 integration modes (OpenAI, Anthropic passthrough, Unified Anthropic) |
| [nefesh-cli](https://github.com/nefesh-ai/nefesh-cli) | Official CLI: `npm install -g @nefesh/cli` |
| [nefesh-sdk](https://github.com/nefesh-ai/nefesh-sdk) | Official TypeScript SDK |
| [human-state-protocol](https://github.com/nefesh-ai/human-state-protocol) | Open specification for human state exchange between AI systems |
| [nefesh-examples](https://github.com/nefesh-ai/nefesh-examples) | Integration examples (Python, JavaScript, curl, Gateway) |
| [nefesh-a2a](https://github.com/nefesh-ai/nefesh-a2a) | A2A v1.0 agent reference implementation |
| [nefesh-wearables](https://github.com/nefesh-ai/nefesh-wearables) | Wearable integration guides |

### Quick start

```bash
# Register a device
curl -X POST https://api.nefesh.ai/v1/devices \
  -H "X-Nefesh-Key: YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"device_name":"My Sensor","device_type":"polar_h10","subject_id":"usr_demo"}'

# Send biometric data
curl -X POST https://api.nefesh.ai/v1/ingest \
  -H "X-Nefesh-Key: YOUR_KEY" \
  -H "Content-Type: application/json" \
  -d '{"device_id":"dev_xxx","heart_rate":72,"timestamp":"2026-01-01T00:00:00Z"}'

# LLM adapts automatically
curl https://gateway.nefesh.ai/v1/chat/completions \
  -H "X-Nefesh-Key: YOUR_KEY" \
  -H "X-Nefesh-Subject: usr_demo" \
  -H "X-LLM-Key: YOUR_LLM_KEY" \
  -d '{"model":"gpt-4o","messages":[{"role":"user","content":"Hello"}]}'
```

Free tier: 1,000 API calls/month, no credit card.

[Get API Key](https://nefesh.ai/signup) | [Documentation](https://nefesh.ai/docs) | [Live Demo](https://sandbox.nefesh.ai) | [Website](https://nefesh.ai)
