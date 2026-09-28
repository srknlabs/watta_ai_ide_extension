<div align="center">

# Watta for VS Code

### Build with an AI coding agent and 200+ models in one IDE

Watta works with your open project: it explores relevant files, answers questions, proposes code changes, and lets you review the result before keeping it.

[![Visual Studio Marketplace](https://img.shields.io/visual-studio-marketplace/v/watta-ai.watta-ai-vscode?style=for-the-badge&logo=visualstudiocode&label=VS%20Code%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode)
[![Installs](https://img.shields.io/visual-studio-marketplace/i/watta-ai.watta-ai-vscode?style=for-the-badge&logo=visualstudiocode&label=Installs)](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode)

**[Install from Marketplace](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode)** · **[Explore Watta](https://watta.io)** · **[View models](https://watta.io/models)** · **[Plans and Energy](https://watta.io/pricing)**

<img src="https://watta.io/apps/vscode/screenshots/overview.png" alt="Watta coding agent in Visual Studio Code" width="880">

</div>

## One workspace, many models

Use **Agent** to explore a codebase and make edits, **Ask** to understand code, or **Plan** to outline a change. Watta Free helps you get started; the model picker also shows Watta Lite, Pro, Max, and compatible models from providers including OpenAI, Anthropic, Google, DeepSeek, Kimi, and Alibaba. Availability, price, and estimated Energy are visible before a request.

| What you can do | How it works |
| --- | --- |
| Work with your project | Search and read relevant files; attach a file or folder to focus the agent. |
| Review changes | See edits in the editor, then accept or revert them. Local checkpoints support recovery. |
| Check the result | Inspect diagnostics for changed files and optionally run a project check script. |
| Keep writing | Get short inline code suggestions from Watta Free. |
| Stay in control | Terminal commands ask for approval; Energy and model access are shown in the picker. |

<div align="center">
<img src="https://watta.io/apps/vscode/screenshots/prompt.png" alt="Prompting the Watta coding agent" width="820">
<br><br>
<img src="https://watta.io/apps/vscode/screenshots/diff-review.png" alt="Reviewing code changes made by Watta" width="820">
</div>

## Get started

1. [Install Watta for VS Code](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode) (VS Code 1.90 or newer).
2. Open the **Watta.io** view and connect your Watta account.
3. Open a project and describe the result you want.
4. Review edits and use **Verify result** before accepting them.

The extension uses your Watta account; separate provider API keys are not required. Inline suggestions can be turned off with `wattaAi.inlineSuggestions.enabled`.

## Downloads and updates

The [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode) is the primary installation channel. Tested VSIX builds will also appear in [GitHub Releases](https://github.com/srknlabs/watta_ai_ide_extension/releases) when published. A newly built VSIX is **not** published here automatically.

## Privacy and support

Watta sends the prompt and code context needed for a request to its service. Tokens are kept in VS Code SecretStorage. Read the [privacy policy](https://watta.io/privacy) and [terms](https://watta.io/terms). For feedback or security concerns, [contact Watta](https://watta.io/contact).

---

This repository is the public product page and release channel for Watta IDE Extension. The extension's source code is proprietary and is not published here. All rights reserved © 2026 Watta.io.
