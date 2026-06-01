<p align="center">
  <img src="docs/public/hero-icon.svg" width="120" height="120" alt="billy-sdk">
</p>

<h1 align="center">billy-sdk</h1>

<p align="center">
  <strong>The easiest AI SDK for Node.js</strong><br>
  Generate, modify, validate, analyze, extract, and execute with natural language prompts.
</p>

<p align="center">
  <a href="https://www.npmjs.com/package/billy-sdk"><img src="https://img.shields.io/npm/v/billy-sdk" alt="npm version"></a>
  <a href="https://www.npmjs.com/package/billy-sdk"><img src="https://img.shields.io/npm/dw/billy-sdk" alt="npm downloads"></a>
  <a href="LICENSE"><img src="https://img.shields.io/npm/l/billy-sdk" alt="License"></a>
  <img src="https://img.shields.io/node/v/billy-sdk" alt="Node version">
  <a href="https://github.com/plinio8899/billy-sdk/actions/workflows/ci.yml"><img src="https://github.com/plinio8899/billy-sdk/actions/workflows/ci.yml/badge.svg" alt="CI"></a>
  <a href="https://plinio8899.github.io/billy-sdk/"><img src="https://img.shields.io/badge/docs-vitepress-blue" alt="Docs"></a>
</p>

---

## Documentation

Full documentation is available at:

### [→ plinio8899.github.io/billy-sdk](https://plinio8899.github.io/billy-sdk/)

Includes guides for installation, providers, methods, type conversion, CLI, and use cases.

---

## Quick Start

```bash
npm install billy-sdk
```

```javascript
import billy from "billy-sdk";

const IA = billy();

await IA.create("genera 10 preguntas sobre la biblia");
console.log(IA.results);
```

## Features

| | |
|---|---|
| **🤖 Multi-Provider** | Groq (default, free), OpenAI, Anthropic — no vendor lock-in |
| **🔄 Type Conversion** | Automatic parsing to number, array, object, boolean, JSON |
| **🧠 Built-in Memory** | `billy({ memory: 10 })` — automatic conversation history |
| **⛓️ Method Chaining** | `IA.asNumber().short().create("prompt")` |
| **🔌 Variable Injection** | `create("prompt {{var}}", { var: value })` |
| **📡 Streaming** | `IA.stream()` — consume responses in real time |
| **📁 File & Image Handling** | Extract text from PDFs and images automatically |
| **🛠️ Tool Calling** | Let the AI call your own functions |
| **⚡ CLI** | `npx billy-sdk config set <key>` |
| **🛡️ Retry & Timeout** | Built-in, configurable |

## One-Minute Setup

```bash
# 1. Install
npm install billy-sdk

# 2. Set API key (Groq is free → https://console.groq.com)
#    Option A: Environment variable (recommended)
export GROQ_API_KEY=gsk_your_key

#    Option B: CLI (saves to ~/.billy-sdk/config.json)
npx billy-sdk config set gsk_your_key

# 3. Use it
echo 'import billy from "billy-sdk"; const IA = billy(); console.log(await IA.create("hola"));' | node
```

## Examples

See the [`examples/`](examples/) directory for 18 runnable scripts: invoice extraction, ticket classification, NL-to-SQL, chatbot, sentiment analysis, email generator, summarizer, content moderation, test data generation, and basic RAG.

## Requirements

- Node.js >= 18
- Internet connection
- API key (Groq offers a free tier)

## License

MIT
