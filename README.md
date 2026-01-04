# 🤖 CodingWithAgent

**Production-ready coding standards and best practices for AI coding agents.**

[![npm version](https://img.shields.io/npm/v/codingwithagent.svg)](https://www.npmjs.com/package/codingwithagent)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Stop fighting with inconsistent AI code output. Get enterprise-grade standards that work across **all major AI coding tools**—Cursor, Windsurf, Google Antigravity, GitHub Copilot, and more.

Turn your AI assistant into a senior engineer that knows your team's rules.

---

## 🚀 Quick Start

Initialize standardized rules in your project with a single command. **No installation required.**

### Using bash

```bash
npx codingwithagent init
```

### Using yarn

```bash
yarn dlx codingwithagent init
```

The interactive CLI will guide you through the setup:

```
🤖 CodingWithAgent
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Production-ready standards for AI coding agents

📋 Choose your profile:

  1. Minimal        Essential rules only (great for getting started)
  2. Standard       Recommended baseline ⭐ (most popular)
  3. Strict         All rules enforced (maximum code quality)
  4. Accessibility  WCAG 2.1+ focused (a11y priority)

Enter number (1-4) [default: 2]: 2

🛠️  Select your AI coding tool:

  1. Cursor           (.cursorrules)
  2. Windsurf         (.windsurfrules)
  3. Antigravity      (.agent/rules/)
  4. GitHub Copilot   (.github/copilot-instructions.md)
  5. Universal        Works with most tools ⭐

Enter number (1-5) [default: 5]: 1

⚙️  Installing...

✨ Created .cursorrules with standard profile
🎉 Setup complete!
```

## 📦 Profiles

Choose the level of enforcement that fits your project maturity.

| Profile              | Description                                                                               | Best For                                     |
| :------------------- | :---------------------------------------------------------------------------------------- | :------------------------------------------- |
| **1. Minimal**       | Essential rules only. Focuses on readability and basic modern patterns.                   | Prototyping, Hackathons, Personal Projects   |
| **2. Standard** ⭐   | **Recommended.** Balanced set of best practices for React, Testing, and Security.         | Most Production Applications                 |
| **3. Strict**        | Maximum enforcement. TypeScript required, 90% test coverage, strict accessible standards. | Enterprise, Fintech, Healthcare, Large Teams |
| **4. Accessibility** | Heavy focus on WCAG 2.1 AA compliance, accessible patterns, and ARIA usage.               | Government, Public Sector, Inclusive Apps    |

## 🛠️ Supported Agents

We standardize instructions across the entire AI ecosystem.

### 1. Cursor (`.cursorrules`)

Generates a comprehensive system prompt file in your project root. Cursor reads this to understand your tech stack, testing requirements, and styling preferences before it writes a single line of code.

### 2. Windsurf (`.windsurfrules`)

Creates a rule file compatible with the Windsurf editor, ensuring your Cascade flows follow your engineering standards.

### 3. Google Antigravity (`.agent/rules/`)

Installs a modular rule set in the `.agent` directory. Antigravity acts as a "Universal" agent and can ingest these specific markdown files (e.g., `accessibility.md`, `testing.md`) to contextually apply rules based on the user's task.

### 4. GitHub Copilot (`.github/copilot-instructions.md`)

Sets up project-specific instructions for GitHub Copilot Chat. This ensures Copilot suggests code that aligns with your specific architectural patterns.

### 5. Universal

A general-format rules file that works with most LLM-based tools that verify context files.

## 🎯 What's Included?

Depending on the profile, your rules will cover:

- **⚡ Tech Stack**: React, TypeScript, Node.js, Next.js patterns.
- **♿ Accessibility**: WCAG 2.1 AA+ compliance, correct ARIA usage, semantic HTML.
- **🧪 Testing**: Unit (Jest/Vitest), Integration, and E2E testing standards.
- **🔒 Security**: Input validation, output sanitization, secret management (OpenSSF aligned).
- **🧠 Anti-Hallucinations**: Instructions to prevent AI from inventing libraries or APIs.
- **📁 File Structure**: component/container architecture, proper folder organization.

## ❓ Troubleshooting

### Error: "InvalidStateError: Failed to register a ServiceWorker"

If you encounter this error when opening the generated rule files in your editor (especially VS Code or strict environments), it is a known issue with the editor's Markdown previewer in restricted modes.

**Solution:**
1. Right-click the file in your explorer.
2. Select **"Open With..."** -> **"Text Editor"** (or similar).
3. The file content is safe standard Markdown. The error is purely a visual bug in the previewer.

## 🤝 Contributing

We welcome community contributions to improve these standards!

1.  Fork the repository.
2.  Add your improvements to the `templates` directory.
3.  Submit a Pull Request.

See [CONTRIBUTING.md](./CONTRIBUTING.md) for detailed guidelines.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
