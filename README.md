# Watta: AI Coding Agent | 300+ AI Models

Describe what you want to build, fix, or improve. Watta works with your project, edits multiple files, and lets you review and undo changes — with 300+ AI models in one account.

## Try 3 paid AI models for free

**[Create your free Watta account and get promo access to 3 paid AI models →](https://watta.io/register?utm_source=extension_readme&utm_medium=referral&utm_campaign=ide_promo)**

The promotional selection rotates, so you can try different models over time. Access is temporary; check the current models and promo limits in Watta before starting. Look for **Temp access** in the model picker.

No separate provider API keys are needed. Install the extension, connect your Watta account, and try your first task in your own project.

### Choose your extension registry

- **[Install from VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=watta-ai.watta-ai-vscode)**
- **[Install from Open VSX](https://open-vsx.org/extension/watta-ai/watta-ai-vscode)**

[Setup guide](https://watta.io/docs/ide/watta-extension) · [Plans and Energy](https://watta.io/dashboard/pricing) · [Privacy](https://watta.io/privacy)

> **Try this first:** “Explain this project and suggest one small improvement. Ask before changing files.”

<p align="center">
  <img src="https://watta.io/apps/vscode/screenshots/overview.png" alt="Watta IDE Extension — describe a task, review code changes, and build in VS Code" width="100%">
</p>

## Build software by describing the result

Open a project, write what you want in plain language, and let Watta work with the codebase already open in your editor. It can inspect files, search the workspace, explain code, suggest a plan, and make edits directly in your files.

Use one account for Watta models and a catalog of 300+ models from leading providers. The model picker shows current availability, pricing, Energy usage, and supported reasoning levels without requiring a separate extension update.

> **For everyday tasks:** “Add a FAQ block to the product page”, “Find why this form does not submit”, or “Explain this file and make the code cleaner.”

## What makes Watta useful

- **A real workspace agent.** Your open project is the working environment. Watta can search, read, and reason across relevant files instead of asking you to copy them into chat.
- **Made for clear requests.** Describe the outcome you want; Agent mode handles the technical steps. Use Ask for explanations and Plan for a proposed approach before editing.
- **Safe, visible edits.** Changes are written and saved so you can see them in the editor immediately, then remain reversible. Accept or undo all changes from the chat, or act next to the changed file.
- **Suggestions where you type.** Enable inline suggestions with one click on **Watta** in the VS Code status bar. Get context-aware code completions as you type and press **Tab** to accept them. Suggestions are off by default, and your choice is remembered. See [Inline code suggestions](#inline-code-suggestions) below.
- **Site preview.** Open an HTML file and run **Watta.io: Preview Site** to view it inside VS Code. You can also enter a running localhost URL.
- **Next edit.** Run **Watta.io: Suggest Next Edit** in a code file to review a small follow-up edit before applying it. Set `wattaAi.nextEdit.enabled` to suggest one automatically after saving.
- **Files and folders as priority context.** Attach from the `+` menu, drag from Explorer, or use **Add File to Chat** from an editor tab. Pinned resources tell the agent where to focus first.
- **300+ models in one place.** Start with Watta Free or choose Watta Lite, Pro, and Max. Use compatible models from providers such as OpenAI, Anthropic, Google, Kimi, DeepSeek, Alibaba, and more.
- **Energy and access are transparent.** See Energy cost, model pricing, and plan/credit availability before you send a request.
- **Keep working while Watta works.** New requests go into a queue by default. You can also stop the current request and run the new one immediately.
- **Follow the agent’s progress.** Brief updates explain its approach and useful findings. Technical steps stay in a collapsed work log under the response, with one current status above the composer while it works. Final answers focus on the result and verification.

## Get started in under a minute

1. Open the **Watta.io** view from the Activity Bar.
2. Select **Connect Watta.io** and finish sign-in in your browser.
3. Open a workspace and write what you need in the composer: **“Describe what you want to build.”**
4. Review the result and keep or undo file changes when you are ready.

No provider API keys are needed: model access, subscription, Energy, and credits are handled through your Watta.io account.

<p align="center">
  <img src="https://watta.io/apps/vscode/screenshots/prompt.png" alt="Start with a simple prompt — describe what you want to build" width="100%">
</p>

## Inline code suggestions

**Turn them on once, then keep typing.** Inline suggestions are **off by default** on a fresh installation. Your choice is remembered across VS Code restarts and extension updates.

1. Sign in to your Watta.io account.
2. Choose a paid or **Temp access** model in Watta chat. Suggestions are unavailable while a free chat model is selected.
3. Click **Watta** in the bottom status bar to enable suggestions. You can also run **Watta.io: Toggle Inline Suggestions** from the Command Palette.
4. Type in a code file. Suggested code appears as ghost text at your cursor; press **Tab** to accept it with VS Code's default keybindings.

Click **Watta** again to turn suggestions off. If the button opens chat, choose an eligible model there and return to your code.

Successful inline suggestions consume **Watta Energy or wallet credits**, using normal Watta Fim pricing. They appear as **Watta Fim** in [Logs](https://watta.io/dashboard/logs) and [Usage](https://watta.io/dashboard/usage). Requests recorded as failed or cancelled are not charged.

Inline completion uses **Watta Fim**, independently of which eligible chat model you choose. It considers code before and after the cursor, the header of a large file, and relevant open files. Suggestions stop when you keep typing, so outdated results do not appear at a moved cursor.

<p align="center">
  <img src="https://watta.io/apps/vscode/screenshots/inline-suggestions.png" alt="Enable Watta inline suggestions from the bottom status bar, type code, and press Tab to accept" width="100%">
</p>

If nothing appears, check that VS Code's **Editor: Inline Suggest: Enabled** setting is on, your workspace is trusted, and you are signed in. Run **Watta.io: Request Inline Suggestion and Show Log** to request a suggestion and open the output channel.

## How editing works

Watta is designed to make code changes understandable and recoverable:

1. The agent reads only the files relevant to your request and reports what it is doing.
2. When it edits a file, the updated content appears in the editor with change highlighting and a compact review in chat.
3. Choose **Accept all** to keep the staged result or **Revert all** to restore the previous content. Per-file controls are also available next to the changed code.
4. Before an agent terminal command runs, Watta asks for approval. You can allow it once or remember the choice for the current workspace.

Watta creates a local checkpoint before approved edits. Use **Watta.io: Restore Last Watta Checkpoint** if you need to roll back the last accepted change set.

<p align="center">
  <img src="https://watta.io/apps/vscode/screenshots/diff-review.png" alt="Review diffs before you apply — accept or reject generated changes" width="100%">
</p>

## Modes and context

| Mode      | Best for                                                             |
| --------- | -------------------------------------------------------------------- |
| **Agent** | Multi-step tasks: inspect, edit, and verify code in the workspace.   |
| **Ask**   | Explain a file, an error, or a piece of code without making changes. |
| **Plan**  | Get a concise implementation plan before asking the agent to edit.   |

The active file and cursor line are included as context when relevant. Pin a specific file or folder when it should take priority over the rest of the workspace.

## Model choice and Energy

The catalog is loaded from Watta.io, so new models, provider names, prices, and availability can appear without updating the extension.

- **Watta Free** is available for getting started.
- **Watta Lite, Pro, and Max** require a Starter plan or higher.
- Other paid models show whether they require a Starter plan and/or account credits.
- Reasoning effort is available as a separate control when the selected model supports it.

## Commands

| Command                                     | Description                                                              |
| ------------------------------------------- | ------------------------------------------------------------------------ |
| **Watta.io: Open Chat**                     | Focus the Watta.io chat view.                                            |
| **Watta.io: Add File to Chat**              | Pin the active file as priority context.                                 |
| **Watta.io: Sign In**                       | Connect your Watta.io account.                                           |
| **Watta.io: Sign Out**                      | Remove the local Watta.io session.                                       |
| **Watta.io: Restore Last Watta Checkpoint** | Restore the latest accepted edit checkpoint.                             |
| **Watta.io: Reset Workspace Approvals**     | Forget remembered file-edit and terminal permissions for this workspace. |

## Settings

| Setting                             | Default                | Description                                                                                                                                                                 |
| ----------------------------------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `wattaAi.agent.maxSteps`            | `8`                    | Maximum agent steps for one request.                                                                                                                                        |
| `wattaAi.agent.enableTerminal`      | `true`                 | Allow the agent to request terminal commands. Every command still needs approval unless you explicitly remember it for the workspace.                                       |
| `wattaAi.inlineSuggestions.enabled` | `false`                | Enable Watta Fim inline completions. The Watta status-bar toggle remembers your choice and takes precedence over this setting. Requires sign-in and an eligible chat model. |
| `wattaAi.apiBaseUrl`                | Watta.io API           | Advanced: override the Watta API endpoint.                                                                                                                                  |
| `wattaAi.authorizationUrl`          | Watta.io authorization | Advanced: override the sign-in endpoint.                                                                                                                                    |

## Privacy and security

- Watta uses OAuth Authorization Code with PKCE.
- Access and refresh tokens are stored only in VS Code `SecretStorage`; they are never exposed to the chat webview.
- Your prompt, selected model, workspace paths, active-editor context, attached resources, and file content needed for a request may be sent to Watta.io to generate a response.
- There is no separate extension telemetry in this release.

Read the full [Privacy Policy](https://watta.io/privacy) and [Terms](https://watta.io/terms). For private security reports, contact [Watta.io support](https://watta.io/contact).

## Requirements

- Visual Studio Code `1.90` or newer.
- A Watta.io account and an internet connection.
- A local or remote workspace for workspace tools. Terminal and Git operations require an environment that supports the VS Code Node.js Extension Host.

## Support

Need help, have product feedback, or want to report a security issue privately? Contact us through [Watta.io support](https://watta.io/contact).

## GitHub downloads

Download tested VSIX builds from [GitHub Releases](https://github.com/srknlabs/watta_ai_ide_extension/releases). This repository is the public product page and release channel. The extension source code is proprietary and is not published here. All rights reserved © 2026 Watta.io.
