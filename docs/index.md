---
layout: home

hero:
  name: "billy-sdk"
  text: "Simple AI for your projects"
  tagline: The easiest way to add AI to your Node.js apps — generate, modify, validate, analyze, extract, and execute with natural language prompts
  image:
    src: /hero-icon.svg
    alt: billy-sdk
  actions:
    - theme: brand
      text: Get Started
      link: /getting-started
    - theme: alt
      text: API Reference
      link: /methods
    - theme: alt
      text: View on GitHub
      link: https://github.com/plinio8899/billy-sdk

features:
  - icon: 🤖
    title: Multi-Provider
    details: Supports Groq (default, free), OpenAI, and Anthropic. No vendor lock-in. Switch providers with one line of code.
    link: /providers
  - icon: 🔄
    title: Type Conversion
    details: Automatic parsing of responses to numbers, arrays, objects, booleans, or JSON. No manual parsing needed.
    link: /types
  - icon: 🧠
    title: Built-in Memory
    details: 'Automatic conversation history via <code>billy({ memory: 10 })</code>. Maintain context across multiple prompts effortlessly.'
    link: /configuration
  - icon: ⛓️
    title: Method Chaining
    details: 'Fluent API — <code>IA.asNumber().short().create("prompt")</code>. Compose behavior with expressive, chainable methods.'
    link: /chaining
  - icon: 🔌
    title: Variable Injection
    details: 'Use <code>{"{{placeholders}}"}</code> in prompts and inject dynamic data at runtime. Template prompts like a pro.'
    link: /variables
  - icon: 📡
    title: Streaming
    details: Real-time streaming responses via <code>IA.stream()</code> with AsyncIterable. Consume chunks as they arrive.
    link: /methods#stream-prompt-variables
  - icon: 📁
    title: File & Image Handling
    details: Extract text from PDFs and images automatically. Pass file paths directly in your prompts.
    link: /files
  - icon: 🛠️
    title: Tool Calling
    details: Let the AI call your own functions. Define tools with schemas and let the model decide when to use them.
    link: /methods
  - icon: ⚡
    title: CLI Ready
    details: Manage your API key with simple CLI commands. No environment variable hassle. <code>npx billy-sdk config set &lt;key&gt;</code>
    link: /cli
  - icon: 🛡️
    title: Retry & Timeout
    details: Built-in retry logic and configurable timeout for production reliability. Your app stays resilient.
    link: /configuration
---

## Quick Start

```bash
npm install billy-sdk
```

```javascript
import billy from "billy-sdk";

const IA = billy();

const response = await IA.create(
  "Generate 5 creative startup ideas in the sustainability space"
);

console.log(response);
```

### One-Minute Setup

```bash
# 1. Set your API key (Groq is free → https://console.groq.com)
export GROQ_API_KEY=gsk_your_key_here

# 2. Run your first prompt
node -e "import billy from 'billy-sdk'; const IA = billy(); IA.create('Say hello!').then(console.log)"
```

> **Tip:** You can also use `npx billy-sdk config set <key>` to save your key globally.

---

### What's Next?

- Dive into the [full documentation](/getting-started)
- Browse [real-world examples](https://github.com/plinio8899/billy-sdk/tree/main/examples) — invoice extraction, chatbots, NL-to-SQL, and more
- Check the [use cases](/use-cases) section for inspiration
