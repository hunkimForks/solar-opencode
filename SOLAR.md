# 🌟 Solar LLM Integration Guide

This guide shows you how to use Upstage's Solar models (solar-pro2 and solar-mini) with opencode.

## 🚀 Quick Start

### 1. Set Up Your API Key

**Option A: Environment Variable (Recommended)**
```bash
export UPSTAGE_API_KEY=up_your_api_key_here
```

**Option B: Interactive Authentication**
```bash
bun run dev auth login
# Select "Upstage" from the provider list
# Enter your API key when prompted
```

### 2. Use Solar Models

**Solar Pro 2 (Most Advanced)**
```bash
# Interactive chat
bun run dev --model upstage/solar-pro2

# Process a file
bun run dev --model upstage/solar-pro2 < myfile.txt

# Direct prompt
echo "Explain quantum computing" | bun run dev --model upstage/solar-pro2
```

**Solar Mini (Fast & Efficient)**
```bash
# For faster responses and lower cost
bun run dev --model upstage/solar-mini "Quick question: What is REST API?"
```

## 📋 Available Models

| Model | Description | Context | Best For |
|-------|-------------|---------|----------|
| `upstage/solar-pro2` | Most intelligent model with reasoning | 65K tokens | Complex tasks, reasoning, analysis |
| `upstage/solar-mini` | Fast and efficient | 32K tokens | Quick responses, simple tasks |

## 🔑 Getting Your API Key

1. Visit [Upstage Console](https://console.upstage.ai/)
2. Sign up or log in to your account
3. Navigate to API Keys section
4. Create a new API key
5. Copy the key (starts with `up_`)

## ⚙️ Configuration

The integration automatically configures:
- **API Endpoint**: `https://api.upstage.ai/v1`
- **Authentication**: Bearer token with your API key
- **Streaming**: Real-time response streaming
- **Format Compatibility**: OpenAI-compatible API format

## 💡 Examples

### Code Analysis
```bash
echo "Analyze this Python code for bugs:" | bun run dev --model upstage/solar-pro2 < script.py
```

### Technical Writing
```bash
bun run dev --model upstage/solar-pro2 "Write API documentation for a user authentication endpoint"
```

### Quick Questions
```bash
bun run dev --model upstage/solar-mini "What's the difference between var, let, and const in JavaScript?"
```

## 🛠️ Troubleshooting

### "Invalid path" Error
- Make sure your API key is correctly set
- Verify the key starts with `up_`

### Type Validation Errors
- This is automatically handled by our streaming response transformer
- If issues persist, try using `solar-mini` first

### Authentication Issues
```bash
# Check stored credentials
bun run dev auth list

# Re-authenticate if needed
bun run dev auth login
```

## 🌐 Resources

- [Upstage Documentation](https://developers.upstage.ai/docs/apis/chat)
- [Solar Pro 2 Model Card](https://huggingface.co/upstage/solar-pro2)
- [Upstage Console](https://console.upstage.ai/)
- [OpenCode Documentation](https://opencode.ai/docs)

## 🤝 Support

For Solar model-specific questions:
- [Upstage Community](https://upstage.ai/community)
- [Upstage Support](https://upstage.ai/support)

For OpenCode integration issues:
- [OpenCode GitHub Issues](https://github.com/opencode-ai/opencode/issues)

---
*Happy coding with Solar! ☀️*