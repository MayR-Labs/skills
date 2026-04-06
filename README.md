# Code Doctrine Skills

A comprehensive, modular collection of senior-level agent skills (plugins) for scaffolding code and enforcing strict architectural standards across languages and frameworks.

## What are Agent Skills?

Agent Skills are specialized instructional bundles designed to inform AI models (like Claude or Gemini) about standard operating procedures, clean architecture rules, and "iron laws" for specific technologies. 

By making these skills available to your AI assistant, it will inherently know precisely how you prefer your code written — avoiding elementary patterns, silent errors, and monolithic "God files" in favor of strict, production-ready, senior-level code.

## 🚀 Installation & Usage

You can install these skills into your project using the standard `skills` CLI toolkit.

To install a specific collection of skills from this repository:

```bash
npx skills add youngmayor/code-doctrine/collection/<category>
```

*(Note: The exact installation commands will depend on your specific agent runner or CLI registry manager).*

## 🏗 Directory Structure

This repository acts as the master registry of all available skills. Skills are categorized into:

- `collection/base/` - Global philosophies, code formatting, anti-patterns.
- `collection/concepts/` - High-level AI workflows (e.g., `eco-mode`).
- `collection/languages/` - Strictly typed and structured architectural rules for programming languages.
- `collection/frameworks/` - UI, routing, and ecosystem-specific best practices.
- `collection/recipes/` - Reusable patterns like Authentication and API Design.

Every skill internally follows the Progressive Disclosure Pattern:
- `SKILL.md`: The entry point containing the core rules and YAML metadata.
- `references/`: In-depth documentation and examples loaded dynamically by the agent.

## 🤝 Contributing

We welcome contributions to expand the Code Doctrine. When adding new skills:
1. Ensure the code conforms to the "Humans First, Machines Second" philosophy.
2. Adhere to the Progressive Disclosure Pattern (entry point `<200 lines`).
3. Include rigorous `references/*.md` providing anti-patterns and their senior-level counterparts.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
