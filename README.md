# Watta: AI Coding Agent & Chats

Build features, fix bugs, and refactor across files in your editor. Choose your AI model and work through one Watta account — no separate provider API keys.

[Install from VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode) · [Install from Open VSX](https://open-vsx.org/extension/watta-ai/watta-ai-vscode)

**[Create your Watta account](https://watta.io/register?utm_source=extension_readme&utm_medium=referral&utm_campaign=ide_onboarding)** · [Setup guide](https://watta.io/docs/ide/watta-extension) · [Pricing](https://watta.io/pricing)

**Agent mode is available on Free, Starter, Pro, and Max.** Workspace tools require a compatible model with tool calling. Free accounts can use eligible free models with their included Energy. Check the model picker for current access, pricing, and available tools.

[![Watta agent working on a coding task](https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/agent.gif)](https://watta.io/apps/vscode/screenshots/20261015-gif-50fps/agent.gif)

*Illustrative demo using a sample project.*

## Get started

1. Install the extension and open a project.
2. Open **Watta** in the Activity Bar, select **Connect Watta.io**, and sign in through your browser.
3. Choose a model and mode, then describe your task. Attach a file or folder to focus the context.

Try in Agent mode: **“Find why this test fails and fix the cause.”**

## What you can do

- **Ask** — chat with your chosen model, explain code, and understand errors.
- **Plan** — investigate the project with read-only tools and work out an approach before editing.
- **Agent** — generate code, edit multiple files, debug, refactor, review code, and run tests.
- **MCP & browser tools** — connect external tools and inspect web pages through **Watta: MCP & Browser Tools**.

## Inline code completion

Inline suggestions are **off by default**. Sign in, select an eligible chat model, and click **Watta** in the status bar to enable them. Press **Tab** to accept a suggestion.

Completion uses **Watta Fim**, independently of the eligible chat model you select. Successful suggestions consume **Energy or wallet credits**. Inline completion is unavailable while a free chat model is selected.

## Your control & privacy

Review file edits and accept or revert them. Restore the latest local checkpoint when needed. Terminal commands and external tool actions require approval; terminal approvals can be remembered for the workspace.

Requests may send your prompt and relevant project context, including code and file paths, to Watta.io. Usage measurements respect VS Code telemetry settings and can be disabled with `wattaAi.telemetry.enabled`.

**Requirements:** VS Code 1.90+ or a compatible editor, a Watta account, and an internet connection. Workspace tools need a trusted project. Browser tools require Chrome on the machine running the extension.

[Documentation](https://watta.io/docs/ide/watta-extension) · [Support](https://watta.io/contact) · [Privacy](https://watta.io/privacy) · [Terms](https://watta.io/terms)

## GitHub downloads

Download tested VSIX builds from [GitHub Releases](https://github.com/srknlabs/watta_ai_ide_extension/releases). This repository is the public product page and release channel. The extension source code is proprietary and is not published here. All rights reserved © 2026 Watta.io.
