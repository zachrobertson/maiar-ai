# Change Log

All notable changes to this project will be documented in this file.  
See [Conventional Commits](https://conventionalcommits.org) for commit guidelines.

# 0.1.1 (2025-02-12)

# 🎉 Introducing Maiar v0.1.1

The initial release of Maiar, a composable, plugin-based AI agent framework.  
This release includes the core framework and official plugins we will support, which include:

- 🧠 Models
- 🔌 Integrations
- 💾 Memory Providers

# 📦 Packages

- ⚙️ Core
  - 🏗 **@maiar-ai/core** - The core framework for building AI agents.
- 🔌 Official Plugins
  - 🧠 Models
    - 🤖 **@maiar-ai/model-openai** - An OpenAI model provider.
    - 🦙 **@maiar-ai/model-ollama** - An Ollama model provider.
  - 🔗 Integrations
    - 🌐 **@maiar-ai/plugin-express** - A plugin for using Maiar with Express.
    - ✍️ **@maiar-ai/plugin-text** - A plugin for text generation capabilities.
    - 🖥️ **@maiar-ai/plugin-terminal** - A plugin for command-line interface interactions.
    - 🔄 **@maiar-ai/plugin-websocket** - A plugin for WebSocket communication.
    - 📩 **@maiar-ai/plugin-telegram** - A plugin for Telegram bot integration.
    - ⏳ **@maiar-ai/plugin-time** - An example plugin for adding time to the agent context.
    - 🖼️ **@maiar-ai/plugin-image** - A plugin for image processing capabilities.
  - 💾 Memory Providers
    - 📂 **@maiar-ai/memory-filesystem** - A filesystem-based memory provider.
    - 🗄️ **@maiar-ai/memory-sqlite** - A SQLite-based memory provider.
